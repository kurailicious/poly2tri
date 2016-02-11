cmake_minimum_required(VERSION 2.8.11)
project(poly2tri)

add_subdirectory(testbed)

include_directories(poly2tri)

add_library(poly2tri 
    poly2tri/poly2tri.h
    poly2tri/common/shapes.h
    poly2tri/common/utils.h
    poly2tri/sweep/advancing_front.h
    poly2tri/sweep/cdt.h
    poly2tri/sweep/sweep_context.h
    poly2tri/common/shapes.cc 
    poly2tri/sweep/advancing_front.cc
    poly2tri/sweep/cdt.cc
    poly2tri/sweep/sweep.cc
    poly2tri/sweep/sweep_context.cc
    )
    
target_include_directories(poly2tri PUBLIC poly2tri)

