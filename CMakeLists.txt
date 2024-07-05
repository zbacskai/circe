cmake_minimum_required(VERSION 3.16 FATAL_ERROR)

project(circe)

set(Boost_USE_STATIC_LIBS OFF) 
set(Boost_USE_MULTITHREADED ON)  
set(Boost_USE_STATIC_RUNTIME OFF) 
set(BOOST_MIN_VERSION "1.71.0")
find_package(Boost REQUIRED) 
find_package(Threads REQUIRED)                                                                                                                                                                                                                

include_directories(${Boost_INCLUDE_DIRS})
add_executable(circe src/main.cpp)
target_link_libraries(circe Boost::boost Threads::Threads)