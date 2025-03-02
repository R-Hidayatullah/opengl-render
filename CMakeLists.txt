cmake_minimum_required(VERSION 3.10)
project(opengl-render VERSION 0.1.0 LANGUAGES C CXX)

# Set C++ standard
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include_directories(include)
include_directories(extern/glad45coreext/include)

# Link GLFW
find_package(glfw3 REQUIRED)

# Add executable
add_executable(opengl-render extern/glad45coreext/src/glad.c src/main.cpp)

target_link_libraries(opengl-render PRIVATE glfw)

