# Camera

A [ROS](http://www.ros.org) node that processes data received from [TeensyCam](https://github.com/icboredman/TeensyCam-HW) - stereo camera module.

Depending on various options defined in [camera.launch](camera.launch), it can generate and broadcast the following ROS topics:
* raw (both left and right) images
* rectified images
* disparity image
* depth image
* camera_info for the above images
* point cloud
* emulated laser scan

This node makes use of [LIBELAS dense stereo library](http://www.cvlibs.net/software/libelas/), specifically its OpenMP-version.

### Prerequisites

#### Serial Communication Library by William Woodall
* get from here: https://github.com/wjwwood/serial
* before `make`, change install location: `cmake -DCMAKE_INSTALL_PREFIX=/opt/serial`
* enable access to serial device: `sudo gpasswd --add ${USER} dialout`
* add to ~/.bashrc: `source /opt/serial/setup.bash`

#### OpenCV
* Version 2.4 or higher

#### OpenMP
* https://www.openmp.org/

#### Boost
* https://www.boost.org/

---
More info about the project is here: https://BoredomProjects.net/index.php/projects/robot-navigation-using-stereo-vision-part-2

