cmake_minimum_required(VERSION 3.22)  # CMake version check
project(simple_opencv)               # Create project "simple_example"
set(CMAKE_CXX_STANDARD 20)            # Enable c++14 standard
add_compile_options(-fvisibility=hidden)

# Add main.cpp file of project root directory as source file
set(SOURCE_FILES main.cpp)

# Add executable target with source files listed in SOURCE_FILES variable
add_executable(simple_example ${SOURCE_FILES})
find_package(OpenCV CONFIG REQUIRED)
target_link_libraries(simple_example PRIVATE opencv_core opencv_highgui opencv_imgproc opencv_photo opencv_imgcodecs) 

