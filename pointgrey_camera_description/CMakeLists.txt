cmake_minimum_required(VERSION 2.8.3)
project(pointgrey_camera_description)

find_program(CCACHE_FOUND ccache)
if (CCACHE_FOUND)
set_property(GLOBAL PROPERTY RULE_LAUNCH_COMPILE ccache)
set_property(GLOBAL PROPERTY RULE_LAUNCH_LINK ccache)
endif(CCACHE_FOUND)

find_package(catkin REQUIRED)

catkin_package()

install(DIRECTORY launch meshes rviz urdf
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
