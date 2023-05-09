# ros_autonomous_slam

## Installation
```bash
sudo apt-get -y install ros-noetic-gazebo-ros-pkgs ros-noetic-gazebo-ros-control ros-noetic-turtlebot3-msgs ros-noetic-turtlebot3 ros-noetic-navigation ros-noetic-gmapping
pip3 install scikit-learn pyyaml
mkdir ~/autoslam_ws/src -p
cd ~/autoslam_ws/src
git clone https://github.com/fazildgr8/ros_autonomous_slam.git
git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations
cd ~/autoslam_ws
catkin_make
```

## Run
* [master branch](https://github.com/jebiio/ros_autonomous_slam) 참조

1. 환경변수 설정
```bash
source ~/autoslam_ws/devel/setup.bash
export TURTLEBOT3_MODEL=waffle_pi
export GAZEBO_MODEL_PATH=<turtlebot3_world model 있는 path>
# ex) export GAZEBO_MODEL_PATH=$GAZEBO_MODEL_PATH:/home/yslee/projects/turtlebot3_ws/src/turtlebot3_simulations/turtlebot3_gazebo/models
```

2. 실행
```bash
roslaunch ros_autonomous_slam turtlebot3_world.launch
```
```bash
# 다른 터미널에서
roslaunch ros_autonomous_slam autonomous_explorer.launch
```
* python script 오류시, python->python3
* rviz에서 publish point안되면, 월드 바꿔보기

