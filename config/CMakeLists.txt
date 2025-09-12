# Debug output
message(STATUS "Processing custom app.cmake")
message(STATUS "CONFIG_ZMK_BEHAVIOR_CAPS_WORD_DE: ${CONFIG_ZMK_BEHAVIOR_CAPS_WORD_DE}")

# Add custom source files
if(CONFIG_ZMK_BEHAVIOR_CAPS_WORD_DE)
    message(STATUS "Adding caps_word_de behavior source file")
    target_sources(app PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/behaviors/behavior_caps_word_de.c)
else()
    message(STATUS "CONFIG_ZMK_BEHAVIOR_CAPS_WORD_DE is not enabled")
endif()
