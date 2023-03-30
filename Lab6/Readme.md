# Choreographing Movement
**List the names and NetID for your partners here.**

Jamie Cao (jc2974), Chenran Ning (cn257), Tingkang Zhao (tz275)

It is about time to have a functioning mobile robot! Starting from this lab, you should prioritize either robot building and/or study design. 

## Prep
### Watch the following tutorials:
- [How to crimp wires](https://www.youtube.com/watch?v=SaU00MMjzn0&ab_channel=GrizzlyBuilds)

- [Beginner's Guide on Soldering](https://www.makerspaces.com/how-to-solder/)


- [How to Solder Wires Together](https://youtu.be/NSqPHQ1zQco)



### For this lab, you will need:
1. Your laptop
2. Cardboard
3. Utility knife
4. Your hoverboard base

### Deliverables for this lab are: 

0. Photos of your robot prototype
1. A video of your robot moving around
2. A sketch of a series movements based on your final project
3. A video showing your robot perform the movements in item #2.
4. Reflect upon your design, what would you do differently?


## Lab Overview
For this assignment, you are going to:

A) [Build your chassis](#part-a-build-your-chassis)

B) [Move it around](#part-b-move-it-around)

C) [Plan a movement](#part-c-plan-a-movement)

D) [Optional Spinning your LiDAR](#part-d-optional-spinning-your-LiDAR)

Labs are due on Tuesdays before class. Make sure this page is linked to on your main class hub page.

## Part A. Build your chassis
If you haven't already, now is a good time to actually mockup a low fidelity version robot for your final project. At least, you should have a chassis that safely host all the hardware you have (ODrive, wheels, battery, etc).

Feel free to use any material we have in lab to build your chassis. Things you might find useful are cardboard, gluegun, zip ties, duo locks, etc. 

## Part B. Move it around
Once you build your chassis, test it out! Power on your hoverboard and connect your controller. Drive your robot around! (Take a video while you do that!)

A few questions to consider:
- when your robot accelerate, is the chassis stable?
- what are all the possible motions (action space) your robot can perform? (e.g. rotating in place, moving foward/backward, ...)
- reflect on your design and think what would you do differently next time.

## Part C. Plan a movement
Based on your scenario, sketch out a sequence of movement in a storyboard format. 
Then, control your robot to execute that sequence of movement. (Take a video while you do that!)


## Part D. Optional spinning your LiDAR
If you plan to use LiDAR for your final project, or are simply curious about how it works, let's set it up!

```
# Install LiDAR SDK
# In your RPi terminal
sudo apt install cmake pkg-config
cd ~
git clone https://github.com/YDLIDAR/YDLidar-SDK.git
cd YDLidar-SDK
mkdir build
cd build
cmake ..
make
sudo make install
```

```
cd ~/mobilehri_ws/src/mobilehri2023
git checkout ydlidar_ros2_driver
cd ~/mobilehri_ws
colcon build

chmod 0777 src/ydlidar_ros2_driver/startup/*
sudo sh src/ydlidar_ros2_driver/startup/initenv.sh

```
Now, plug in your LiDAR.
```
# start your LiDAR
source install setup.bash
ros2 launch ydlidar_ros2_driver ydlidar_launch.py 
```

To visualize your LiDAR reading, open foxglove studio in vnc viewer. Then, click 3D in the left panel.

### Again, deliverables for this lab are: 

0. Photos of your robot prototype
1. A video of your robot moving around
2. A sketch of a series movements based on your final project
3. A video showing your robot perform the movements in 2.
4. Reflect upon your design, what would you do differently?

## Deliverables

0. Photos of your robot prototype
    
    [Front side photo](https://drive.google.com/file/d/1VkesMxyO7Z1RiHMWY6ALWCOseT6hezc1/view?usp=sharing)
    
    [Back side photo](https://drive.google.com/file/d/1if_7-2htfUN7T-2U6KTGvuIf_W8f2ucd/view?usp=sharing)

1. A video of your robot moving around

    We haven't got swivel wheels for our robot, so it cannot maintain balance by itself right now. We will fix this as soon as we meet Frank to ask for the wheels in the next lab session.
    
    [Video](https://drive.google.com/file/d/1makx8e2Jteu94M9LYDhXuEwZEfG5Gi2q/view?usp=sharing)

2. A sketch of a series movements based on your final project
    
    Our final project idea is a (hopefully voice-controled) moving furniture. So there are no special moves accociated with our special project, only the basics:
    
    a. Move forward and backward
    
    [Move forward and backward sketch](https://drive.google.com/file/d/1crexxD9H-y0uTZJQfejxDFTJwZZhRvHN/view?usp=sharing)
    
    b. Change direction
    
    [Change direction sketch](https://drive.google.com/file/d/1SMy33jgRTWeTbizC7Jrk2-3zFU1TGOtb/view?usp=sharing)
    
    
3. A video showing your robot perform the movements in 2.
    
    As we stated earlier, there are no special moves accociated with our special project, only the basics. So the video here is the same as the video in 2.
    
    [Video](https://drive.google.com/file/d/1makx8e2Jteu94M9LYDhXuEwZEfG5Gi2q/view?usp=sharing)
    
5. Reflect upon your design, what would you do differently?

    I would add one or two additional swivel wheels to help our robot maintain its balance.
