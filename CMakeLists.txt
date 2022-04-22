cmake_minimum_required(VERSION 3.20)
project(boost_test)

set(CMAKE_CXX_STANDARD 11)

find_package(Boost 1.78.0 COMPONENTS system filesystem REQUIRED)
include_directories(${Boost_INCLUDE_DIRS})
set(SOURCE_FILES main.cpp)
add_executable(boost_test ${SOURCE_FILES})
target_link_libraries(boost_test ${Boost_LIBRARIES})

#add_executable(boost_test main.cpp)