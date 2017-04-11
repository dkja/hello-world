cmake_minimum_required(VERSION 3.0.0)

set(CMAKE_CXX_STANDARD "14")

if(CMAKE_BUILD_TYPE STREQUAL "Debug")
    set(CMAKE_CXX_FLAGS "-g")
endif()
if(CMAKE_BUILD_TYPE STREQUAL "Release")
    set(CMAKE_CXX_FLAGS "-O2")
endif()

project(hello_proj)

file(GLOB srcs "${CMAKE_SOURCE_DIR}/src/*.cpp")
include_directories("${CMAKE_SOURCE_DIR}/include")



add_executable(hello_proj ${srcs})
# target_link_libraries(hello_proj )