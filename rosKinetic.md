## How to visualize a rosbag data (camera +LiDAR) in rviz, specifically the camera ovelay on LiDAR data  
Terminal 1:

```
$ roscore
```
Terminal 2:

```
$ rosrun tf static_transform_publisher 0 0 0 0 0 0 velodyne camera_optical 10
```

Terminal 3:

```
$ rosparam set use_sim_time true
$ rosrun rviz rviz
```

Terminal 4:

```
$ rosbag play -l yourBagFile.bag --clock
```

