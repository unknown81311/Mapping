cmake_minimum_required(VERSION 3.20.0)
project(MAPPING)

add_library(Mapping INTERFACE)

add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/modules/ScrapMechanic/")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/modules/Lua/")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/modules/Steam/")

target_link_libraries(Mapping INTERFACE ScrapMechanic)
target_link_libraries(Mapping INTERFACE Lua)
target_link_libraries(Mapping INTERFACE Steam)
