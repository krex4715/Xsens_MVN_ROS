cmake_minimum_required(VERSION 2.8.3)
project(xsens_receiver)


find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  message_generation
)

 add_message_files(
   FILES
   xsens_data.msg
 )

 generate_messages(
   DEPENDENCIES
   std_msgs
 )

catkin_package(
 CATKIN_DEPENDS roscpp rospy message_runtime
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

