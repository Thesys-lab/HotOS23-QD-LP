
add_executable(cachesim main.c cli.c cli_parser.c params.c sim.c ../cli_utils.c)
target_link_libraries(cachesim ${ALL_MODULES} ${LIBS} ${CMAKE_THREAD_LIBS_INIT} utils)
install(TARGETS cachesim RUNTIME DESTINATION bin)

add_executable(filter filter.c cli.c cli_parser.c params.c sim.c ../cli_utils.c)
target_link_libraries(filter ${ALL_MODULES} ${LIBS} ${CMAKE_THREAD_LIBS_INIT} utils)
install(TARGETS filter RUNTIME DESTINATION bin)

add_executable(flash flash.cpp cli.c cli_parser.c params.c sim.c ../cli_utils.c)
target_link_libraries(flash ${ALL_MODULES} ${LIBS} ${CMAKE_THREAD_LIBS_INIT} utils)
