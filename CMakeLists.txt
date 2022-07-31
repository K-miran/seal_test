# Copyright (c) Microsoft Corporation. All rights reserved.
# Licensed under the MIT license.

cmake_minimum_required(VERSION 3.13)

project(HEtest VERSION 1.0 LANGUAGES CXX)

add_compile_options(-O2)
add_compile_options(-std=c++17)
add_compile_options(-march=native)
add_compile_options(-g)

add_executable(test "main.cpp")
#add_executable(sol "solution.cpp")

# Import Microsoft SEAL
find_package(SEAL 4.0.0 EXACT REQUIRED)

target_link_libraries(test SEAL::seal)
#target_link_libraries(sol SEAL::seal)