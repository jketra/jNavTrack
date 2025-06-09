cmake_minimum_required(VERSION 3.22)
project(JNavTrack)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

find_package(Qt6 6.5 COMPONENTS REQUIRED Core Quick)
message(STATUS "Using Qt ${Qt6Core_VERSION}")

add_executable(JNavTrack
    simulator/Dynamics.cpp
    simulator/KalmanPredictor.cpp
    simulator/main.cpp
    interface/ViewModel.cpp
    ui/main.qml
)

target_link_libraries(JNavTrack Qt6::Core Qt6::Quick)
