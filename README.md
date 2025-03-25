# A System for Multi-View Mapping of Dynamic Scenes Using Time-Synchronized UAVs

This repository contains all the software and hardware design used for our paper - [A System for Multi-View Mapping of Dynamic Scenes Using Time-Synchronized UAVs]. The system is designed to map dynamic scenes using multiple UAVs. The UAVs are equipped with a stereo camera. The system is capable of mapping dynamic scenes in real-time and can be used for applications such as Human Motion Capture in the wild, Sports Analytics, CGI, etc.

![System Overview](assets/overview.png)

## Hardware Setup
We use the following hardware components for our system:
- [Ublox F9T GPS Module](https://www.sparkfun.com/sparkfun-gnss-timing-breakout-zed-f9t-qwiic.html)
- [Multi Band GNSS Antenna]()
- [BlackFly S BFS-U3-16S2C](https://www.teledynevisionsolutions.com/products/blackfly-s-usb3/?model=BFS-U3-16S2C-CS&vertical=machine%20vision&segment=iis)
- [Nvidia Jetson Orin Nano]()
- [Pixhawk 4 mini]()
- [Sync Board]()
- [Mesh Radio]()
- [Drone Frame]()

## Software Setup
Our software runs on ROS1 and is tested on Ubuntu 20.04. We use the following ROS packages:
- [mavros]()
- [mavros_extras]()
- [spinnaker_camera_driver]()
- [GPS_driver]()

For 3D and 4D reconstruction, we use the following codebases:
- [COLMAP]()
- [VGGSFM]()

## Dataset
We provide a dataset of dynamic scenes captured using our system. The raw dataset can be downloaded from [here]()
The dataset folder contains the following:
- Rosbag files of the stereo camera and GPS data.
- Calibration files for the stereo camera.

We also provide the processed dataset [here]()
The processed dataset contains the following:
- Extracted images, timestamps, and GPS data.
- Small sequences of images for 4D reconstruction. Each sequence contains the following:
    - Rectified stereo images.
    - Stereo disparity maps.
    - Stereo depth maps.
    - Generated 3D point cloud from depth maps.
    - Aligned GPS data.
    - 3D reconstruction using VGGSFM for each timestep.
    - 4D reconstruction using VGGSFM and COLMAP for the sequence.



