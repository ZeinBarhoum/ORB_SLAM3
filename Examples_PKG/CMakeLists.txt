cmake_minimum_required(VERSION 3.0)
project(orb_slam_example_pkg)

set(CMAKE_CXX_STANDARD 14)

list(APPEND CMAKE_PREFIX_PATH "~/Programs/source/ORB_SLAM3/install/cmake")
find_package(ORB_SLAM3 REQUIRED)

include_directories( ${ORB_SLAM3_INCLUDE_DIRS})

add_executable(mono_euroc src/mono_euroc.cpp)
target_link_libraries(mono_euroc ${ORB_SLAM3_LIBRARIES})
