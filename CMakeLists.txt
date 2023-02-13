cmake_minimum_required(VERSION 3.16)

project(qttest VERSION 1.0.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)

find_package(Qt6 REQUIRED COMPONENTS Widgets)

add_executable(qttest
    window.h
    window.cpp
    main.cpp
)

target_link_libraries(qttest PRIVATE Qt6::Widgets)

set_target_properties(qttest PROPERTIES
    WIN32_EXECUTABLE ON
    MACOSX_BUNDLE ON
)
