# provide libcanard/*.h for the app
zephyr_interface_library_named(canard)
target_include_directories(canard INTERFACE ${ZEPHYR_CURRENT_MODULE_DIR})

# provides libcanard.a for zephyr.elf (thus for libapp.a)
zephyr_library()
zephyr_library_sources(${ZEPHYR_CURRENT_MODULE_DIR}/libcanard/canard.c)
