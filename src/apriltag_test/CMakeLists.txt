cmake_minimum_required(VERSION 3.0.0)

project(apriltag_test)

 set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wno-narrowing")

set(CMAKE_CXX_STANDARD 11) # Tell CMake to compile with C++11

find_package(catkin REQUIRED COMPONENTS
  roscpp
  roslib
  sensor_msgs
  geometry_msgs
  tf
)

catkin_package(
  INCLUDE_DIRS include
  CATKIN_DEPENDS roscpp geometry_msgs tf
  DEPENDS
)

include_directories(
  include
  /usr/include/eigen3
  ${catkin_INCLUDE_DIRS}
)

set(SRC_LIST
)

# add_executable(${PROJECT_NAME}
#   ${SRC_LIST}
# )

# add_dependencies(${PROJECT_NAME}
#   ${${PROJECT_NAME}_EXPORTED_TARGETS}
#   ${catkin_EXPORTED_TARGETS}
# )

# target_link_libraries(${PROJECT_NAME}
#   ${catkin_LIBRARIES}
# )
