cmake_minimum_required(VERSION 3.8)

project(cherno)

add_subdirectory(glew-cmake)
add_subdirectory(glfw)

add_executable(test
    main.cpp
)

target_include_directories(test PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/glfw/include)
target_include_directories(test PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/glew-cmake/include)

target_link_libraries(test glfw libglew_static)