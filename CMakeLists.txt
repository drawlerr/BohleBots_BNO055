set(CMAKE_TOOLCHAIN_FILE cmake/Arduino-Toolchain.cmake) # Arduino Toolchain

cmake_minimum_required(VERSION 3.8)

project(BohleBots_BNO055)
get_board_id(board_id uno atmega328)

add_arduino_executable(${PROJECT_NAME} ${board_id} src/BohleBots_BNO055.cpp)

link_platform_library(${PROJECT_NAME} EEPROM ${board_id})
