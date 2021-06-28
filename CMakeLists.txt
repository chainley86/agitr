# What version of CMake is needed?
cmake_minimum_required(VERSION 2.8.3)

# Name of this package.
project(agitr)

# Find the catkin build system, and any other packages on
# which we depend.
find_package(catkin REQUIRED COMPONENTS roscpp geometry_msgs)

# Declare our catking package.
catkin_package()

# Specify locations of header files.
include_directories(include ${catkin_INCLUDE_DIRS})

# Declare executable, along with its source files.  If
# there are multiple exectuables, use multiple copies of
# this line.
add_executable(hello hello.cpp)
add_executable(pubvel pubvel.cpp)

# Specify libraries against which to line.  Again, this
# line should be copied for each distince exectuable in
# this pacakge.
target_link_libraries(hello ${catkin_LIBRARIES})
target_link_libraries(pubvel ${catkin_LIBRARIES})