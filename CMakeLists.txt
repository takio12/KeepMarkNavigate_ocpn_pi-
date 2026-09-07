cmake_minimum_required(VERSION 3.16)
project(KeepMarkNavigate_ocpn_pi)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(KeepMarkNavigate_ocpn_pi SHARED
    src/plugin.cpp
)

target_include_directories(KeepMarkNavigate_ocpn_pi PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)

if(WIN32)
    target_compile_definitions(KeepMarkNavigate_ocpn_pi PRIVATE _CRT_SECURE_NO_WARNINGS)
endif()
