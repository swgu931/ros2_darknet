# ros2_darknet with realsense camera

## reference for nvidia driver install
- ref: https://codechacha.com/ko/install-nvidia-driver-ubuntu/

## making working directory

mkdir ~/darknet_ros2_ws
cd ~/darknet_ros2_ws
mkdir src
cd src

## download source code to build
git clone https://github.com/ros2/openrobotics_darknet_ros
git clone -b ros2 https://github.com/ros-perception/vision_msgs
git clone https://github.com/ros2/darknet_vendor

## reference to use intel realsense camera  
- https://github.com/intel/ros2_intel_realsense

git clone https://github.com/intel/ros2_intel_realsense

## build without CUDA
cd ~/darknet_ros2_ws
colcon build --symlink-install --cmake-args -DDARKNET_CUDA=Off -DDARKNET_OPENCV=Off

