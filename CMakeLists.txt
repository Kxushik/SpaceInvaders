cmake_minimum_required(VERSION 3.30)
project(spaceinvaders)

set(CMAKE_CXX_STANDARD 20)
# Find and link GLFW
find_package(glfw3 REQUIRED)
find_package(OpenGL REQUIRED)

#Add Glew
find_library(GLEW_LIBRARY glew REQUIRED)
include_directories(/usr/local/include)

add_executable(spaceinvaders main.cpp)
target_link_libraries(spaceinvaders glfw OpenGL::GL ${GLEW_LIBRARY})