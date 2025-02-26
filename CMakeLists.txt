cmake_minimum_required(VERSION 3.10)
project(BufferOverflowDemo)

set(CMAKE_CXX_STANDARD 11)

add_executable(BufferOverflowDemo 
    BufferOverflow.cpp
    fail.cpp
)

# Enable warnings
if (MSVC)
    target_compile_options(BufferOverflowDemo PRIVATE /W4)
else()
    target_compile_options(BufferOverflowDemo PRIVATE -Wall -Wextra -pedantic)
endif()
