cmake_minimum_required(VERSION 3.11.3)

set(CMAKE_CXX_STANDARD 17)

project(Membot)

set(wxWidgets_ROOT_DIR "C:\\Program Files (x86)\\wxWidgets")
set(wxWidgets_LIB_DIR "C:\\Program Files (x86)\\wxWidgets\\lib\\gcc_x64_dll")
find_package(wxWidgets REQUIRED COMPONENTS core base)
include(${wxWidgets_USE_FILE})

file(GLOB project_SRCS src/*.cpp)

add_executable(membot ${project_SRCS})
target_link_libraries(membot ${wxWidgets_LIBRARIES})
target_include_directories(membot PRIVATE ${wxWidgets_INCLUDE_DIRS})
