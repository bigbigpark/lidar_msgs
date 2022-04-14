cmake_minimum_required(VERSION 3.0.2)
project(lidar_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  roscpp
  rospy
  std_msgs
  geometry_msgs
)

add_message_files(
  FILES
  Curb.msg
  Lane.msg
  PointStamped.msg
  box.msg
  BoxInfo.msg
  SocketBox.msg
)
generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)
catkin_package(
 CATKIN_DEPENDS message_runtime std_msgs geometry_msgs
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)
