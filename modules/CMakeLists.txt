###
### Compile fortran module sources
###
set(SOURCES
    global_variables_${BUILD_TARGET}.f90
    timelog.f90
    env_variables.f90
    opt_variables.f90
    performance_analyzer.f90
    env_variables_internal.c
    papi_wrap.c
    nvtx.f90
    communication.f90
    )
#if (USE_NVTX)
#   set(SOURCES ${SOURCES} nvtx.f90)
#endif ()
add_library(${MODULE_LIB} STATIC ${SOURCES})
