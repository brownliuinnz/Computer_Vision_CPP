


cmake_minimum_required(VERSION 3.0.0)
project(brown VERSION 0.1.0)

include(CTest)
enable_testing()

add_executable(brown main.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)




cmake_minimum_required(VERSION 3.9)

set(PROJECT_NAME TestOpenCVCmake)
project(${PROJECT_NAME})

set(CMAKE_CXX_STANDARD 11)

find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(TestOpenCVCmake main.cpp)

target_link_libraries(${PROJECT_NAME} ${OpenCV_LIBS})