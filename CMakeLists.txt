cmake_minimum_required(VERSION 2.8)
if(POLICY CMP0020)
        cmake_policy(SET CMP0020 NEW) # Drop when CMake >= 2.8.11 required
endif()

project(QtGoogleAnalytics)

if(MSVC)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /Wall /Wx")
else(MSVC)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++0x")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Werror")
endif(MSVC)

set(QtGoogleAnalytics_HEADERS
    ${CMAKE_CURRENT_SOURCE_DIR}/src/QtGoogleAnalytics.h)

add_subdirectory(src)
add_subdirectory(tests EXCLUDE_FROM_ALL)
