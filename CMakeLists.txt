cmake_minimum_required(VERSION 2.8.12)

project(object_keypoint_msgs)

set(CMAKE_CXX_FLAGS "-std=c++11 ${CMAKE_CXX_FLAGS}")

find_package(catkin REQUIRED
  COMPONENTS
    std_msgs
    message_generation
)

add_message_files(
  FILES
    Point2D.msg
    KeyPoint.msg
    ObjectKeyPoints.msg
    ObjectKeyPointArray.msg    
)

generate_messages(
  DEPENDENCIES
    std_msgs
)

catkin_package(
  CATKIN_DEPENDS
    std_msgs
    message_runtime
)
