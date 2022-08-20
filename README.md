# ROS-Robot-arm
## Steps to install and run the arm package on the ROS system:
### open terminal and write following commands:
### 1 - Catkin Workspace:
```
mkdir -p ~/catkin_ws/src

cd ~/catkin_ws/

catkin_make

echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc

source ~/.bashrc
```

<div>
<img src="https://user-images.githubusercontent.com/109974986/185767720-e8c0a026-4c51-4a15-bb00-61aa6886e12c.jpg" width="300">
  </div>
  
  ### Dependencies in ROS:
  ```
  cd ~/catkin_ws/src

git clone https://github.com/smart-methods/arduino_robot_arm.git 

cd ~/catkin_ws

rosdep install --from-paths src --ignore-src -r -y

sudo apt-get install ros-noetic-moveit

sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui

sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher

sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
```
### Compile the package: 
```
catkin_make
```
<div>
<img src="https://user-images.githubusercontent.com/109974986/185768055-58725f33-4f86-4e3f-a307-2c598a2f5f4b.jpg" width="300">
  </div>
  
  ### The command to operate the arm pack:
  ```
  roslaunch robot_arm_pkg check_motors.launch
  ```
  <div>
<img src="https://user-images.githubusercontent.com/109974986/185768164-80c65775-0f74-41b8-baa6-7c24d7251dcd.jpg" width="500">
  </div>
  
