cmake_minimum_required (VERSION 2.6)
project(densecrf)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${PROJECT_SOURCE_DIR}/cmake)

find_package(Eigen3 REQUIRED)
find_package(lbfgs REQUIRED)

include_directories(
	include
	${EIGEN3_INCLUDE_DIRS}
	${lbfgs_INCLUDE_DIRS}
)

add_subdirectory(src)
add_subdirectory(examples)
