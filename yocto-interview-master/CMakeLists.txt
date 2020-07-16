CMAKE_MINIMUM_REQUIRED (VERSION 2.8.6)
project(motesque-eigen)

set( CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_SOURCE_DIR})

#list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/eigen3/Eeigen3/Eigen)

if(UNIX)
	SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -std=gnu++11 -I/usr/include/eigen3")
endif()

#find_package(EIGEN REQUIRED)

#${EIGEN_INCLUDE_DIRS}

include_directories(${CMAKE_SOURCE_DIR})

add_executable(motesque-eigen main.cpp)

install(TARGETS motesque-eigen
        RUNTIME DESTINATION /usr/local/bin/)
