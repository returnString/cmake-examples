cmake_minimum_required(VERSION 3.7)

project(hello-world)

if(MSVC)
	add_compile_options(/W4 /WX)
elseif(CMAKE_CXX_COMPILER_ID MATCHES "Clang")
	add_compile_options(-Werror -Weverything)
endif()

add_executable(hello-world
	main.cpp
)