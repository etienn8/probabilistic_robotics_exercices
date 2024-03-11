cmake_minimum_required(VERSION 3.10)

# C++11
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

## Variables
set(PROBABILIY_LIB proba_rob_lib)

## Project meta data
project(probabilistic_robotics_exercices VERSION 1.0)

# Include directories
include_directories(include)

## Add libraries
add_library(${PROBABILIY_LIB} 
    src/bayes_filter.cpp
)

## Executables 
add_executable(e1_2 src/e1_2.cpp)

target_link_libraries(e1_2 ${PROBABILIY_LIB})
