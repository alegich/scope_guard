cmake_minimum_required(VERSION 3.6)

set(TARGET_NAME scope-guard-test)

project(${TARGET_NAME})

set(CMAKE_CXX_STANDARD 14)

add_definitions(-Wall -Werror -Wextra -Wpedantic -Wnon-virtual-dtor)

set(CMAKE_EXE_LINKER_FLAGS "-Wl,--fatal-warnings")

set(SOURCE_FILES
  ut/scope_guard_test.cpp
)

set(HEADER_FILES
	include/scope_guard.h
)

add_executable(${TARGET_NAME} ${SOURCE_LIST} ${HEADER_LIST})

