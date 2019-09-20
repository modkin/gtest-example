cmake_minimum_required( VERSION 3.10 )
project(gtestMinimal)
set(CMAKE_CXX_STANDARD 11)

#this adds googltest
add_subdirectory(gtest)

add_library(factorial factorial.cc)
add_library(prime prime.cc)

add_executable(testFactoriaAndPrime testFactorialAndPrime.cc)
target_link_libraries(testFactorialAndPrime gtest gtest_main factorial prime)
