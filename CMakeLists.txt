cmake_minimum_required(VERSION 3.4)

project(CubeFile)

# Find Python
find_package(PythonLibs REQUIRED)

# C++11
set(CMAKE_CXX_STANDARD 11)

# Include Directory for pybind11
include_directories(${PYTHON_INCLUDE_DIRS} ${PYBIND_INCLUDE})

# SOURCES and SHARED Library
set(SOURCES CubeFile-pybind11.cpp CubeFile.cpp)
add_library(CubeFile SHARED ${SOURCES})
set_target_properties(CubeFile PROPERTIES PREFIX "")
