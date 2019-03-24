This package has been developed in ROS-kinetic. 
For mapping and map interaction gmapping and map_server can be used.
Make sure this packages are installed using the command
rospack find <package_name>


This package essentially simulates a differential mobile robot with two drive wheels and 4 caster wheels and a laser on top in thw willow garage world.

The robot description is available in urdf/general_diff_drive.urdf.xacro. It has base_link with description of the robot and visuals imported from the dae. Two wheel joints driven by a ros_differential controller through the topic /cmd_vel of type geometry_msgs/Twist.
The description also publishes tf, odom and laser_scan in appropriate formates(http://www.ros.org/reps/rep-0105.html)
base_link frame, odom frame and laser frame are present.
The name of laser scan topic is /scan.



Sequence of running the simulations to map the environment.
1. cd workspace_ws/
2. source devel/setup.bash
3. roslaunch mapping_gazebo_sim diff_drive.launch
4. roslaunch gmapping slam_gmapping_pr2.launch

 Now the robot is ready to run and mapping can be started. The robot takes /cmd_vel of type geometry_msgs/Twist. key_teleop package can be used to send commands after making appropriate changes in the topic name.








