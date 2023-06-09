cmake_minimum_required(VERSION 3.16)
project(lion-zcbor)

# cppcheck crashes on these: disable for now
unset(CMAKE_C_CPPCHECK)

add_library(lion-zcbor)

target_sources(lion-zcbor PRIVATE
    src/zcbor_common.c
    src/zcbor_decode.c
    src/zcbor_encode.c)
target_include_directories(lion-zcbor PUBLIC include)