##############################################################################
# CMake
##############################################################################

cmake_minimum_required(VERSION 2.8.3)
project(pyros_schemas)

##############################################################################
# Find Packages
##############################################################################

find_package(catkin REQUIRED COMPONENTS
    catkin_pip
    std_msgs
)

##############################################################################
# Catkin
##############################################################################

catkin_pip_package(pyros_schemas)

#########
# Tests
#######

if (CATKIN_ENABLE_TESTING)
  catkin_add_pytests(tests/test_pyros_schemas)
endif()


