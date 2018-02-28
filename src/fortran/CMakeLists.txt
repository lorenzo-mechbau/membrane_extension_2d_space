add_executable(${ExampleName} ${ExampleName}.F90)
target_compile_options(${ExampleName} PRIVATE -ffpe-trap=invalid,zero,overflow)
target_link_libraries(${ExampleName} PRIVATE opencmisslibs)

install(TARGETS ${ExampleName} DESTINATION bin)

configure_file(visualise.cmgui visualise.cmgui)

