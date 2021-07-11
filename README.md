# SLAM-map-navigation 
## Using SLAM map to launch the navigation -  Task 5 for track AI at Smart-Methods summer training

### Steps 
- Launch Simulation World:
```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
```
- Run Navigation Node:
```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
```
- Estimate Initial Pose
1. click on the 2D Pose Estimate button in the RViz menu.
2. click on the map where the actual robot is located and drag the arrow toward the direction where the robot is facing.
3. Repeat step 1 and 2 until the LDS sensor data is overlayed on the saved map.
4. Launch keyboard teleoperation node to precisely locate the robot on the map:
```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
5. Move the robot back and forth a bit to collect the surrounding environment information and narrow down the estimated location of the TurtleBot3 on the map which is displayed with tiny green arrows.
6. Terminate the keyboard teleoperation node by entering Ctrl + C

- Set Navigation Goal
1. Click the 2D Nav Goal button in the RViz menu.
2. Click on the map to set the destination of the robot and drag the green arrow toward the direction where the robot will be facing.

### Results 
![navigation](Task4.PNG)
</br>
**Video**
</br>
![Vid](AI-Task4.mp4)
