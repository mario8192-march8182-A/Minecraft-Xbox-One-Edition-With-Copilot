cmake_minimum_required(VERSION 3.10)

project(MinecraftXboxOneEdition CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Find Vulkan
find_package(Vulkan REQUIRED)
include_directories(${Vulkan_INCLUDE_DIRS})

# Find GLFW
find_package(glfw3 REQUIRED)
include_directories(${GLFW_INCLUDE_DIRS})

# Find GLM
find_package(glm REQUIRED)
include_directories(${GLM_INCLUDE_DIRS})

add_executable(Minecraft main.cpp) # Replace 'main.cpp' with your actual source files

# Link libraries
target_link_libraries(Minecraft Vulkan::Vulkan glfw glm)