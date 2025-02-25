cmake_minimum_required(VERSION 3.20)
project(led_test)

add_library(led_test)
target_compile_options(led_test PRIVATE -Wall -Wextra)
set_target_properties(led_test PROPERTIES C_STANDARD 11)

target_include_directories(led_test PUBLIC include)
add_subdirectory(src)

file(CONFIGURE OUTPUT .gitignore
  NEWLINE_STYLE UNIX
  CONTENT "*")
