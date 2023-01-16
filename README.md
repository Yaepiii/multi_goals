# multi_goals
With this feature pack, you can select multiple target navigation points through rviz's `Point` tool, and once you have selected them, the robot will go to each target point in turn

# Requirement
The package has been tested on both ROS Noetic, The following requirements are needed before installing the package:

1- You should have installed a ROS distribution (Noetic or later).

2- Created a workspace.

3- Installed the "gmapping" or other SLAM ROS package: on Ubuntu, and if you are running ROS Noetic, you can do that by typing the following command in the terminal:
```
$ sudo apt-get install ros-noetic-gmapping
```
4- Install ROS navigation stack. You can do that with the following command (assuming Ubuntu, ROS Noetic):
```
$ sudo apt-get install ros-noetic-navigation
```

# Installation
Download the package and place it inside the `/src` folder in your workspace. And then compile using `catkin_make`.

# Run
1-The `slam_view.launch` file in the `/launch` folder launches the pre-configured SLAM node, the move_base node, and the rviz interface. When you start a simulated environment or run the driver on a real robot, you can launch these nodes with the following command.

```
roslaunch multi_goals slam_view.launch
```

2-You can then use the following command to start the multiobjective navigation program:

```
roslaunch multi_goals multi_goals.launch
```

3-Click `Publish Point` at the top of RViz.

4-Select a series of goals

5-After that you'll see a series of Straight path.

6-Do the step 3 once again, then this time click near the last point.

7-Finally, multiobjective navigation start.

