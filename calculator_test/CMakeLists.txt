cmake_minimum_required(VERSION 3.2)
project(calculator_test1)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -O3")

add_subdirectory(lib/googletest)

include_directories(${DIVISION_HEADERS_DIR})
include_directories(lib/googletest/googletest/include)
include_directories(../calculator)

add_executable(calculator_test calculator_test.cpp)
target_link_libraries(calculator_test calculator gtest gtest_main)
