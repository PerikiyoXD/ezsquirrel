file(GLOB_RECURSE SQUIRREL_STDLIB_SOURCES "src/*.cpp")

add_library(sqstdlib STATIC ${SQUIRREL_STDLIB_SOURCES})

target_link_libraries(sqstdlib squirrel)

install(TARGETS sqstdlib RUNTIME DESTINATION ${INSTALL_BIN_DIR}
                         LIBRARY DESTINATION ${INSTALL_LIB_DIR}
                         ARCHIVE DESTINATION ${INSTALL_LIB_DIR})
