cmake_minimum_required(VERSION 3.13)

if(ESP_PLATFORM)
  file(GLOB_RECURSE LORAWAN_ESP32
    "src/*.*"
  )

  idf_component_register(
    SRCS ${LORAWAN_ESP32} 
    INCLUDE_DIRS src 
    REQUIRES RadioLib arduino
  )

  return()
endif()
