# Find Zephyr. This also loads Zephyr's build system.
cmake_minimum_required(VERSION 3.13.1)

IF(BOARD STREQUAL "esp32")
    add_compile_definitions(ESP32)
ENDIF()

find_package(Zephyr)
project(d39_fuel_flow)

# Add application code
target_sources(app PRIVATE src/main.c)
