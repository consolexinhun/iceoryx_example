cmake_minimum_required(VERSION 3.16)
project(example_icehello)

set(ROOT ${CMAKE_CURRENT_SOURCE_DIR})

# find_package(iceoryx_platform REQUIRED)
find_package(iceoryx_posh CONFIG REQUIRED)
# find_package(iceoryx_hoofs CONFIG REQUIRED)


add_executable(pub ${ROOT}/hello_pub.cpp)
target_link_libraries(pub iceoryx_posh::iceoryx_posh)

add_executable(sub ${ROOT}/hello_sub.cpp)
target_link_libraries(sub iceoryx_posh::iceoryx_posh)