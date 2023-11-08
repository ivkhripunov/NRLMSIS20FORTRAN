# CMake project file for NRLMSIS

cmake_minimum_required (VERSION 2.6)
project (NRLMSIS)
enable_language (Fortran)

add_compile_options(-DDBLE -march=native -ffast-math)

file(GLOB_RECURSE SOURCE *.F90)
add_executable (NRLMSIS ${SOURCE} msis20.parm)

