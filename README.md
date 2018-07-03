# SLAM-Project

This robot can be controlled manually with teleop to create a 3D map of its environment and a 2D occupancy grid map with the RTABMap library.

## Setup Instructions
**Clone the repository**
```
//in the src directory of your catkin workspace
$ git clone https://github.com/vixtah/SLAM-Project
$ cd ..
$ catkin_make
$ source devel/setup.bash
```

## Example
Start world and setup keyboard teleop
```
$ roslaunch slam_project world.launch world_file:=/home/nvidia/catkin_ws/src/slam_project/worlds/kitchen_dining.world
$ roslaunch slam_project teleop.launch
```

Start mapping
```
$ roslaunch slam_project mapping.launch simulation:=true 2>/dev/null &
$ roslaunch slam_project rviz.launch 2>/dev/null

```
