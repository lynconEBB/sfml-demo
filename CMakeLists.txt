cmake_minimum_required(VERSION 3.25)
project(sfmlgame)
set(CMAKE_CXX_STANDARD 17)

include(CMakePrintHelpers)
add_executable(sfmlgame main.cpp)

set(BUILD_SHARED_LIBS false)
add_subdirectory(lib/SFML)
target_include_directories(sfmlgame PRIVATE lib/SFML/include)

target_link_libraries(sfmlgame PRIVATE sfml-window sfml-graphics)