# Exercise Session 1

[Exercise Session 1.pdf](Exercise%20S%202ae5f/Exercise_Session_1.pdf)

Directory system for project

```bash
cd ~/ros_workspaces/eth_smb_ws
cd ~/git
```

## Solution 1:

```bash
sudo apt-get install ros-noetic-hector-gazebo-plugins
sudo apt-get install ros-noetic-velodyne-description

cd ~/git
# unzip/clone working files

cd ~/ros_workspaces
mkdir eth_smb_ws
cd ~/ros_workspaces/eth_smb_ws
mkdir src
mkdir logs

cd ~/ros_workspace/eth_smb_ws/src 
ln -s /git/smb_common
cd ..
catkin build smb_gazebo
source devel/setup.bash

roslaunch smb_gazebo smb_gazebo.launch
```

- Install required packages
- Clone required files
- Make workspace
- symlink require files
- Build workspace
- Source workspace
- Launch ROS file

launches gazebo with smb

![Untitled](Exercise%20S%202ae5f/Untitled.png)

## Solution 2

- rostopic list

```bash
rafay@omen:~$ rosnode list
/base_controller_spawner
/gazebo
/gazebo_gui
/rosout
/smb_robot_state_publisher
```

- rostopic list

```bash
rafay@omen:~$ rostopic list
/clock
/cmd_vel
/gazebo/link_states
/gazebo/model_states
/gazebo/parameter_descriptions
/gazebo/parameter_updates
/gazebo/performance_metrics
/gazebo/set_link_state
/gazebo/set_model_state
/gazebo_ros_control/pid_gains/LF_WHEEL_JOINT/parameter_descriptions
/gazebo_ros_control/pid_gains/LF_WHEEL_JOINT/parameter_updates
/gazebo_ros_control/pid_gains/LH_WHEEL_JOINT/parameter_descriptions
/gazebo_ros_control/pid_gains/LH_WHEEL_JOINT/parameter_updates
/gazebo_ros_control/pid_gains/RF_WHEEL_JOINT/parameter_descriptions
/gazebo_ros_control/pid_gains/RF_WHEEL_JOINT/parameter_updates
/gazebo_ros_control/pid_gains/RH_WHEEL_JOINT/parameter_descriptions
/gazebo_ros_control/pid_gains/RH_WHEEL_JOINT/parameter_updates
/imu0
/imu0/accel/parameter_descriptions
/imu0/accel/parameter_updates
/imu0/bias
/imu0/rate/parameter_descriptions
/imu0/rate/parameter_updates
/imu0/yaw/parameter_descriptions
/imu0/yaw/parameter_updates
/joint_states
/odom
/rosout
/rosout_agg
/smb_velocity_controller/cmd_vel
/smb_velocity_controller/odom
/smb_velocity_controller/parameter_descriptions
/smb_velocity_controller/parameter_updates
/tf
/tf_static
```

- rqt_graph

![Untitled](Exercise%20S%202ae5f/Untitled%201.png)