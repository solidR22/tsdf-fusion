cmake_minimum_required(VERSION 3.10)
project(tsdf LANGUAGES CUDA CXX)

include(CheckLanguage)
check_language(CUDA)

find_package(OpenCV 4 REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(tsdf demo.cu)
target_link_libraries(tsdf ${OpenCV_LIBS})
