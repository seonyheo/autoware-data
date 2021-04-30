# autoware-data for LG SVL Automotive Simulator

This repository contains additional data files and scripts needed to run Autoware with LG SVL's Automotive Simulator. 

It includes any data files such as point cloud maps, vector maps, and calibration files. It also contains launch scripts to bring up Autoware compatible with currently available environments in the simulator.

## Support for Multiple Cameras

For my research, I modified the original autoware data to test multi-camera object detection on Autoware.

## Vehicle Configurations

Please use the following vehicle configurations for the LGSVL simulator to enable multiple cameras.

### BorresgasAve

- Lexus2016RXHybrid

```
[{"type": "GPS Device", "name": "GPS", "params": {"Frequency": 12.5, "Topic": "/nmea_sentence", "Frame": "gps", "IgnoreMapOrigin": true}, "transform": {"x": 0, "y": 0, "z": 0, "pitch": 0, "yaw": 0, "roll": 0}},
{"type": "GPS Odometry", "name": "GPS Odometry", "params": {"Frequency": 12.5, "Topic": "/odom", "Frame": "gps", "IgnoreMapOrigin": true}, "transform": {"x": 0, "y": 0, "z": 0, "pitch": 0, "yaw": 0, "roll": 0}},
{"type": "IMU", "name": "IMU", "params": {"Topic": "/imu_raw", "Frame": "imu"}, "transform": {"x": 0, "y": 0, "z": 0, "pitch": 0, "yaw": 0, "roll": 0}},
{"type": "Lidar", "name": "Lidar", "params": {"LaserCount": 32, "MinDistance": 0.5, "MaxDistance": 100, "RotationFrequency": 10, "MeasurementsPerRotation": 360, "FieldOfView": 41.33, "CenterAngle": 10, "Compensated": true, "PointColor": "#ff000000", "Topic": "/points_raw", "Frame": "velodyne"}, "transform": {"x": 0, "y": 2.312, "z": -0.3679201, "pitch": 0, "yaw": 0, "roll": 0}},
{"type": "Color Camera", "name": "Main Camera", "params": {"Width": 1920, "Height": 1080, "Frequency": 15, "JpegQuality": 75, "FieldOfView": 50, "MinDistance": 0.1, "MaxDistance": 2000, "Topic": "/simulator/camera_node/image/compressed", "Frame": "camera_main"}, "transform": {"x": 0, "y": 1.7, "z": -0.2, "pitch": 0, "yaw": 0, "roll": 0}},
{"type": "Color Camera", "name": "Left Camera", "params": {"Width": 1920, "Height": 1080, "Frequency": 15, "JpegQuality": 75, "FieldOfView": "transform": {"x": -0.8, "y": 0.8, "z": 0, "pitch": 0, "yaw": 270, "roll": 0}},
{"type": "Color Camera", "name": "Right Camera", "params": {"Width": 1920, "Height": 1080, "Frequency": 15, "JpegQuality": 75, "FieldOfView": 50, "MinDistance": 0.1, "MaxDistance": 2000, "Topic": "/simulator/camera_node_right/image/compressed", "Frame": "camera_right"}, "transform": {"x": 0.8, "y": 0.8, "z": 0, "pitch": 0, "yaw": 90, "roll": 0}},
{"type": "Keyboard Control", "name": "Keyboard Car Control"},{"type": "Wheel Control", "name": "Wheel Car Control"},{"type": "Vehicle Control", "name": "Autoware Car Control","params": {"Topic": "/vehicle_cmd"} }]
```

# Copyright and License

Copyright (c) 2018 LG Electronics, Inc.

This software contains code licensed as described in LICENSE.

 
