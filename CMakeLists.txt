# Top
cmake_minimum_required(VERSION 3.0.0)
project(FastMRICPP VERSION 0.1.0)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include(${CMAKE_SOURCE_DIR}/conan/conanbuildinfo.cmake)
conan_basic_setup()

# include(CMake/GTKmm.cmake)
include(CMake/wxWidgets.cmake)

include_directories(include)
add_subdirectory(src)

# include(CTest)
enable_testing()
add_subdirectory(tests)


set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
