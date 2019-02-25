cmake_minimum_required(VERSION 3.10)
project(mrfplusplus)

INCLUDE_DIRECTORIES(/usr/local/include/hidapi)
LINK_DIRECTORIES(linux/.libs)

set(CMAKE_CXX_STANDARD 14)

add_executable(mrfplusplus mrfpp.cpp)
TARGET_LINK_LIBRARIES(mrfplusplus hidapi-hidraw)