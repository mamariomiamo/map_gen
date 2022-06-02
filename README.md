__Credits:__
Most of code was adapted from https://github.com/HKUST-Aerial-Robotics/FUEL/tree/main/uav_simulator/map_generator

__Notes:__
Generated map will be published to `/map_generator/global_cloud`

__Parameters:__
**map/radius**: change the square window size
**map/wall_height**: change the height of the wall
**map/len2**: change the thickness of the wall
**map/window_height**: change the center of the window to (0, 0, `map/wall_height`)
**map/resolution**: change the resolution of the cloud

### Generate random forest
`roslaunch map_generator map_gen.launch`

### Generate wall with window
`roslaunch map_generator wall_with_window.launch`

### Generate new map
`roslaunch map_generator click_map.launch`

### Save pointcloud to pcd file
`rosrun map_generator map_recorder /PATH_TO_WHERE_TO_SAVE`
This will save a pcd file called **tmp.pcd** to `/PATH_TO_WHERE_TO_SAVE`.

### Publish pointcloud from pcd
`roslaunch map_generator pcd2cloud.launch pcd_file:=/PATH_TO_YOUR_PCD_FILE`
This will publish pointcloud message to `/map_generator/global_cloud`. Can be used together with swam-playground.
