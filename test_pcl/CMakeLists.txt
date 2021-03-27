cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

project(test_pcl)

find_package(PCL 1.2 REQUIRED)

include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (cloud_viewer cloud_viewer.cpp)
target_link_libraries (cloud_viewer ${PCL_LIBRARIES})

add_executable (cloud_visualization main.cpp)
target_link_libraries (cloud_visualization ${PCL_LIBRARIES})

add_executable (cloud_writer cloud_writer.cpp)
target_link_libraries (cloud_writer ${PCL_LIBRARIES})

add_executable (writer_viewer writer_viewer.cpp)
target_link_libraries (writer_viewer ${PCL_LIBRARIES})

