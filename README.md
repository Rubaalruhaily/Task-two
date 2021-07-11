# This task aims to simulate the way the robot discovers its' environment in Gazebo using SLAM.

1.Install ROS
 ```
$ sudo apt update
$ sudo apt upgrade
$ wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros_melodic.sh
$ chmod 755 ./install_ros_melodic.sh 
$ bash ./install_ros_melodic.sh
 ```
 2.Install dependencey Package
 ```
$ sudo apt-get install ros-melodic-joy ros-melodic-teleop-twist-joy \
$ ros-melodic-teleop-twist-keyboard ros-melodic-laser-proc \
$ ros-melodic-rgbd-launch ros-melodic-depthimage-to-laserscan \
$ ros-melodic-rosserial-arduino ros-melodic-rosserial-python \
$ ros-melodic-rosserial-server ros-melodic-rosserial-client \
$ ros-melodic-rosserial-msgs ros-melodic-amcl ros-melodic-map-server \
$ ros-melodic-move-base ros-melodic-urdf ros-melodic-xacro \
$ ros-melodic-compressed-image-transport ros-melodic-rqt* \
$ ros-melodic-gmapping ros-melodic-navigation ros-melodic-interactive-markers
```
3.Install Turtlebot3 Packages

```
$ sudo apt-get install ros-melodic-dynamixel-sdk
$ sudo apt-get install ros-melodic-turtlebot3-msgs
$ sudo apt-get install ros-melodic-turtlebot3

```
4.Simulation Install

```
$ cd ~/catkin_ws/src/
$ git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
$ cd ~/catkin_ws && catkin_make
$ source ~/catkin_ws/devel/setup.bash
$ cd
```
5. Launch Simulation World

```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch

```
6.Run SLAM Node

```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping

```
7.Run Teleoperation Node

```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

```
8.Project's Photos 

![5](https://user-images.githubusercontent.com/86341464/125203646-f2f91200-e281-11eb-9415-97858fa3508a.PNG)

9.MAP
![6](https://user-images.githubusercontent.com/86341464/125203655-01472e00-e282-11eb-891e-09998fcb68cc.PNG)

