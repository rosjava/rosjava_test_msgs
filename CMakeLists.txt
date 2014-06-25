##############################################################################
# CMake
##############################################################################

cmake_minimum_required(VERSION 2.8.3)
project(rosjava_test_msgs)

##############################################################################
# Dependencies
##############################################################################

find_package(catkin REQUIRED COMPONENTS message_generation std_msgs)

##############################################################################
# Messages
##############################################################################

add_message_files(
  DIRECTORY msg
  FILES
  Composite.msg
  CompositeA.msg
  CompositeB.msg
  TestArrays.msg
  TestHeader.msg
  TestPrimitives.msg
  TestString.msg
)


add_service_files(
  DIRECTORY srv
  FILES
  AddTwoInts.srv
)


generate_messages(DEPENDENCIES std_msgs)

##############################################################################
# Package
##############################################################################

catkin_package(
  CATKIN_DEPENDS message_runtime std_msgs
)
