cmake_minimum_required(VERSION 2.8.3)
project(robot_commander_tsn11)

find_package(catkin_simple REQUIRED)

catkin_simple()

# example boost usage
# find_package(Boost REQUIRED COMPONENTS system thread)

# C++0x support - not quite the same as final C++11!
# SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++0x")

# Libraries
# cs_add_libraries(my_lib src/my_lib.cpp)   

# Executables
cs_add_executable(robot_commander_tsn11 src/robot_commander.cpp)
cs_add_executable(halt_commander_tsn11 src/halt_commander.cpp)
cs_add_executable(vel_scheduler_tsn11 src/vel_scheduler.cpp)
cs_add_executable(simple_vel_scheduler_tsn11 src/simple_vel_scheduler.cpp)
# target_link_library(example my_lib)
 
cs_install()
cs_export()