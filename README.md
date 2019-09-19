# Localization_amcl
Robot Navigation and localization in a mapped environment using Gazebo , ROS packages , amcl, Rviz. Two different robot models are used to test the navigation and localisation. 
For more details refer **https://github.com/shwetaruparel/Localization_amcl/blob/master/Localization_amcl.pdf**

# Abstract
      Mobile robot localization is a challenge of determining a robot’s pose from sensor data in a mapped environment.
      Often the robots are required to be able to navigate and get the information about its surrounding. 
      Autonomous navigation or along the way-points the robot must be able to perceive its surrounding and make localization decision.

# Steps to download and create a ROS environment.

### Create catkin_workspace directory in /home/workspace
      $ mkdir ~/home/workspace/create_ws/src
      $ cd /home/workspace/catkin_ws/src/
      $ catkin_create_pkg udacity_bot
      $ cd udacity_bot
### Next, download all the folders and CMakeLists.txt(replace one already present) directly into udacity_bot package
### Next, compile all the componenets.
      $ cd /home/workspace/catkin_ws
      $ catkin_make
      $ source devel/setup.bash
      
### Next open three terminals and run Gazebo, rviz and check the navigation using the provided goal file.
      $ roslaunch udacity_bot udacity_world.launch
      $ roslaunch udacity_bot amcl.launch
      $ rosrun udacity_bot navigation_goal
      
### Next change the udacity_bot.xacro file with the safety_bot.xacro file , but save it as udacity_bot.xacro, and then run Gazebo,rviz and provided Goal just like the above step. This robot has a different model(a cylinderical base).


# Check the Localization.pdf for detailed analysis of Localization and localization algorithms (EKF and AMCL)
