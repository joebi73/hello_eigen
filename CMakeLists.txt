cmake_minimum_required(VERSION 3.11)
project(HelloEigen CXX)
set(CMAKE_CXX_EXTENSIONS OFF) # OFF -> -std=c++14, ON -> -std=gnu++14
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED true)

find_package(Eigen3 3.4 REQUIRED NO_MODULE)
if (Eigen3_FOUND)
  message("Eigen3 is found")
elseif(Eigen3_FOUND)
  message("Eigen3 is not found")
endif(Eigen3_FOUND)

add_executable(HelloEigen main.cpp) 
target_link_libraries(HelloEigen Eigen3::Eigen)

