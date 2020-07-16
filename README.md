# SLAM-approach-and-simulation
In computational geometry, simultaneous localization and mapping is the computational problem of constructing or updating a map of an unknown environment while simultaneously keeping track of an agent's location within it.

-------

This tutorial is for Gazebo simulation.
You need first to install Turtlebot3 package if you did not install it check this link now
- https://github.com/Memo5679/Running-ROS-turtlebot3-robot-simulation.

--------------------------

# SLAM-Turtlebot3-simulation- (ROS Kinetic)
### If you haven't downloaded Turtlebot3 packages you may find them in the link below
###### https://emanual.robotis.com/docs/en/platform/turtlebot3/pc_setup/
## In the beginning, we are gonna run Gazebo World in order to see the map
#### The used world is Turtlebot3 House and the used turtlebot model is burger.
```ruby
export TURTLEBOT3_MODEL=burger
```
```ruby
roslaunch turtlebot3_gazebo turtlebot3_house.launch
```
## In order to control a TurtleBot3 with a keyboard. Open new terminal.
```ruby
export TURTLEBOT3_MODEL=burger
```
```ruby
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
## Thirdly, open new terminal and export the robot model and run the SLAM node in RViz.
```ruby
export TURTLEBOT3_MODEL=burger
```
```ruby
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
```
## Lastly. After moving around the map. If you want to save the map in .pgm & .yml
```ruby
rosrun map_server map_saver -f ~/map
```
##### You will find the saved map in home directory

**********************

--------------------------------
# write this command to get the map
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping

Creating Indoor map with Stimultneous Localization and Mapping (SLAM) and Gmapping with turtlebot3.

--------

First, install turtlebot3 simulation packages.

Then, run the following commands:

- launch gazebo world with a turtlebot.

```ruby
roslaunch turtlebot3_gazebo turtlebot3_world.launch
```

--------

- launch SLAM with rviz and spacify gmapping method.

```ruby
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
```
--------

- launch key teleop to cover the whole area.

```ruby
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
-------

- when you finish, save the map using map_server package.

```ruby
rosrun map_server map_saver -f ~/map
```
