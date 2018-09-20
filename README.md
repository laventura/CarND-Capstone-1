Team: Millenium Vulkan
============

🤖🚙 This is the capstone project for Udacity's Self Driving Car Nanodegree. 

The gif below shows our code deployed on Udacity's (actual) self driving car nicknamed _Carla_. Carla was tested in a small parking lot, and was supervised by a trained engineer from Udacity. I sat shotgun and filmed the sequence. 👍The car drives autonomously and properly stops at a (fake) traffic light when it turns red. 
[![Carla](https://github.com/laventura/blog_fyi/blob/master/static/images/aa-sdc.gif)](https://github.com/laventura/blog_fyi/blob/master/static/images/aa-sdc.gif)

*Update (Oct 2017)* I graduated the Self-Driving Car Nanodegree 🎉🍾. Here's a brief I wrote on my blog [atul.fyi](https://atul.fyi/post/2017/10/22/graduated-self-driving-car-nanodegree/)
 
### Team Members

This repository is maintained by the following:
- George Terzakis 
- Martin Herzog
- Yuda Liu 
- Atul Acharya
- Yoni Azuelos


The following video shows the code in action:

[![Capstone](http://img.youtube.com/vi/1KDDv5UTwig/0.jpg)](http://www.youtube.com/watch?v=1KDDv5UTwig "CarND Capstone Project")

### Usage

1. Clone the project repository
```bash
git clone https://github.com/herzogmartin/CarND-Capstone.git
```

2. Clone the team's submodule
```bash
cd CarND-Capstone
git submodule init
git submodule update

git pull origin master
```

3. Install python dependencies
```bash
pip install -r requirements.txt
```
4. Make and run styx
```bash
cd ros
catkin_make
source devel/setup.sh
roslaunch launch/styx.launch
```
5. Run the simulator

### Native Installation

* Be sure that your workstation is running Ubuntu 16.04 Xenial Xerus or Ubuntu 14.04 Trusty Tahir. [Ubuntu downloads can be found here](https://www.ubuntu.com/download/desktop).
* If using a Virtual Machine to install Ubuntu, use the following configuration as minimum:
  * 2 CPU
  * 2 GB system memory
  * 25 GB of free hard drive space

  The Udacity provided virtual machine has ROS and Dataspeed DBW already installed, so you can skip the next two steps if you are using this.

* Follow these instructions to install ROS
  * [ROS Kinetic](http://wiki.ros.org/kinetic/Installation/Ubuntu) if you have Ubuntu 16.04.
  * [ROS Indigo](http://wiki.ros.org/indigo/Installation/Ubuntu) if you have Ubuntu 14.04.
* [Dataspeed DBW](https://bitbucket.org/DataspeedInc/dbw_mkz_ros)
  * Use this option to install the SDK on a workstation that already has ROS installed: [One Line SDK Install (binary)](https://bitbucket.org/DataspeedInc/dbw_mkz_ros/src/81e63fcc335d7b64139d7482017d6a97b405e250/ROS_SETUP.md?fileviewer=file-view-default)
* Download the [Udacity Simulator](https://github.com/udacity/CarND-Capstone/releases/tag/v1.2).

### Docker Installation
[Install Docker](https://docs.docker.com/engine/installation/)

Build the docker container
```bash
docker build . -t capstone
```

Run the docker file
```bash
docker run -p 127.0.0.1:4567:4567 -v $PWD:/capstone -v /tmp/log:/root/.ros/ --rm -it capstone
```

### Real world testing
1. Download [training bag](https://drive.google.com/file/d/0B2_h37bMVw3iYkdJTlRSUlJIamM/view?usp=sharing) that was recorded on the Udacity self-driving car (a bag demonstraing the correct predictions in autonomous mode can be found [here](https://drive.google.com/open?id=0B2_h37bMVw3iT0ZEdlF4N01QbHc))
2. Unzip the file
```bash
unzip traffic_light_bag_files.zip
```
3. Play the bag file
```bash
rosbag play -l traffic_light_bag_files/loop_with_traffic_light.bag
```
4. Launch your project in site mode
```bash
cd CarND-Capstone/ros
roslaunch launch/site.launch
```
5. Confirm that traffic light detection works on real life images
