cmake_minimum_required(VERSION 3.5)

project(MultipleObjectTracking LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# OpenCV:
FIND_PACKAGE(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})
link_directories(${OpenCV_LIBRARY_DIR})

add_executable(${PROJECT_NAME} main.cpp blob.cpp blob.h)

target_link_libraries(${PROJECT_NAME} ${OpenCV_LIBRARIES})
