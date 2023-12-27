# CMakeLists.txt
cmake_minimum_required(VERSION 3.12)
project(DesignForge)

# Add the GLFW library
add_subdirectory(deps/glfw)

# Add the source files
add_executable(DesignForge src/main.cpp)

# Include GLFW headers
target_include_directories(DesignForge PRIVATE deps/glfw/include)

# Link against the GLFW library
target_link_libraries(DesignForge glfw)
