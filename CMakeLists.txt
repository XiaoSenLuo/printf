cmake_minimum_required(VERSION 3.19.0)
add_library(printf STATIC)
target_compile_definitions(printf PRIVATE PRINTF_INCLUDE_CONFIG_H)
target_include_directories(printf PUBLIC
        "${CMAKE_CURRENT_SOURCE_DIR}"
)

target_sources(printf PRIVATE
        "printf.c"
)

target_link_libraries(printf PRIVATE FreeRTOS)
