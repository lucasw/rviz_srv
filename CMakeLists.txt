cmake_minimum_required(VERSION 2.8.11.2)
project(rviz_srv)

find_package(catkin REQUIRED
  COMPONENTS
  message_generation
  visualization_msgs
)

add_service_files(
  FILES AddMarker.srv
)

generate_messages(
  DEPENDENCIES
  visualization_msgs
)

catkin_package(
  # INCLUDE_DIRS
  # LIBRARIES
  CATKIN_DEPENDS
    message_runtime
    visualization_msgs
)

