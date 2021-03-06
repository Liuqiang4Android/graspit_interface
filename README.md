graspit_interface
=================

This plugin exposes a ROS interface for the GraspIt! simulator via [graspit-ros](https://github.com/graspit-simulator/graspit-ros). The main purpose for writing this plugin was to demonstrate what we believe is the easiest way to expose GraspIt!
functionality as a variety ROS services and action servers. 

Please feel free to use this as a template to write your own bridge between your ros system and GraspIt!.

To see how a client interacts with this interface, check out our python client
[graspit_commander](https://github.com/graspit-simulator/graspit_commander).


Setup:
------
```
//create ros workspace
mkdir -p graspit_ros_ws/src
cd graspit_ros_ws/src

source /opt/ros/indigo/setup.bash
catkin_init_workspace . 

//clone packages
git clone https://github.com/graspit-simulator/graspit-ros.git --recursive
git clone https://github.com/graspit-simulator/graspit_interface.git
git clone https://github.com/graspit-simulator/graspit_commander.git

//build workspace
cd graspit_ros_ws
catkin_make
```


Launching graspit_interface:
-------
```
source devel/setup.bash
roslaunch graspit_interface graspit_interface.launch
```

Then you can view available services and topics provided by the graspit_interface via:
```
rostopic list
rosservice list
```
