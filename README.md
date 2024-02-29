# sia-labrover
Code for the SIA Lab ROSMASTER R2 setup

## ROS2 Setup

This device came with ROS1 melodic pre-installed in an environment

First unplug the yahboom USB.  Next install a ROS2 image on the usb.

the ROS2 Image can be installed here [ROS2 ROSMASTER R2](https://drive.google.com/drive/folders/1nyf-BhgrBftryZCUAIYJwh2Tsl45R1Ju?usp=drive_link)
 or can be found by scrolling to the bottom of the page on yahbooms [website](http://www.yahboom.net/study/ROSMASTER-R2) and use the link there (System file for NANO-ROS2)

Next use SDFormatter to format the flash drive.  Then use Win32 or an image installer such as balenaEtcher to upload the image onto the drive.

Once the image is installed add it to the yahboom car and power on.  
There is an app startup that runs, first disable this.  

Open Ubuntu system applications, search Startup Applications, remove the check mark in front of start_rosmaster_app as shown in the following figure to close the large program permanently.

Next run the docker container on the image to start ROS2.  

I was running into issues where the /dev/astradepth device could not be found.  If you run into this issue unplug and replug the camera and this device should show up.  To make sure run 

```sh
ls /dev | grep astra
```

and you should see 

```
astradepth
astrauvc
```
show up



