cmake_minimum_required(VERSION 2.8)

set(NAME "vxwx-rlogind")

project(${NAME})

set(CMAKE_CXX_FLAGS "-O3 -Wall -s -std=c++11")
set(CMAKE_C_FLAGS "-O3 -Wall -s -std=c11")

set(DIRS
)

file(GLOB SRC *.cpp *.c)

foreach(ELEM ${DIRS})
    file(GLOB_RECURSE FILES ${ELEM}.cpp ${ELEM}.c)
    list(APPEND SRC ${FILES})
endforeach(ELEM)

add_executable(${NAME}.out ${SRC})

