cmake_minimum_required(VERSION 3.10)
project(window C)

set(CMAKE_C_STANDARD 99)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/../bin)

include_directories(${CMAKE_SOURCE_DIR}/../raylib/include)
link_directories(${CMAKE_SOURCE_DIR}/../raylib/lib)

add_executable(${PROJECT_NAME} main.c)

target_link_libraries(${PROJECT_NAME} raylib winmm gdi32 opengl32)
