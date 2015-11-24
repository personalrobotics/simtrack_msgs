cmake_minimum_required(VERSION 2.8.3)
project(simtrack_msgs)
find_package(catkin REQUIRED COMPONENTS std_msgs sensor_msgs geometry_msgs message_generation)

add_service_files(FILES
  DetectObjects.srv
  EnableService.srv
  SwitchCamera.srv
  SwitchObjects.srv
)

generate_messages(DEPENDENCIES std_msgs sensor_msgs geometry_msgs)

catkin_package(CATKIN_DEPENDS message_runtime std_msgs sensor_msgs geometry_msgs)
