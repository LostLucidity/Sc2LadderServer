# Debug Bot source files
file(GLOB SOURCES_SC2LADDERSERVER_DEBUGBOT "*.cpp" "*.h")

# Include directories
include_directories(SYSTEM
    ${PROJECT_SOURCE_DIR}/tests/debugbot
    ${PROJECT_SOURCE_DIR}/cpp-sc2/include
    ${PROJECT_BINARY_DIR}/cpp-sc2/generated
)

# Create the executable.
add_executable(DebugBot ${SOURCES_SC2LADDERSERVER_DEBUGBOT})
target_link_libraries(DebugBot
    sc2api sc2lib sc2utils
)