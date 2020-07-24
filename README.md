# Turtlebot3-Inastallation

In this tutorial the installation of Turulebot3 on ROS-NOETIC will be addressed. 
Turtlebot3 is an open source simulater tool with a small, affordable, programmable and ROS based robot.
It has three models of robots Burger, which is the basic model, Waffle and Waffle Pi. The difference between the two models is that the Waffle is bigger, has more sensors, and more powerful servos to drive the wheels and handle more payload. In this tutorial, the burger model is used because of its simplacity and basic model. 

In order to install tutrlebot3 first you need to intsall ROS on Ubunto. 
Open the command window; 
1. Source your work with catkin:
  $ source /opt/ros/noetic/setup.bash
2. Create a folder for your workspace in ROS:
  $ mikdr -p ~/catkin_ws/src/
3. Go to the src folder to start installing-write the commands each in sepret lines:
  $ cd ~/catkin_ws/src/
  $ git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
    if you do not have 'git' command installed you may need to install it using the command $ sudo apt install git-all
  $ git clone https://github.com/ROBOTIS-GIT/turtlebot3.git
  $ cd ~/catkin_ws && catkin_make
4. Now to source the directory and shows your turtlebot3 model:
  $ gedit ~/.bashrc
  Go to the bottom of the file and wirte these two lines:
    $ source ~/catkin_ws/devel/setup.bash
    $ export TURTLEBOT3_MODEL=burger
  Then save and exit the file and type the below command to reload.bashrc
  $ source ~/.bashrc
5. Now to install turtlebot3 simulation files:
  $ cd ~/catkin_ws/src/
  $ git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
  $ cd ~/catkin_ws && catkin_make
  
  Now you have successfully install turtlebot3 simualtion tool! 
  
  To launch the robot using RViz use the following commands:
    You need to source your directory every time you want to run the simulator. 
      $ source ~/catkin_ws/devel/setup.bash
      $ export TURTLEBOT3_MODEL=burger
  $ roslaunch turtlebot3_fake turtlebot3_fake.launch 
  and to move the robot around the screen, open new terminal and type the following:
  $ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
  for the instruction keys follow the commands. 
  
  
