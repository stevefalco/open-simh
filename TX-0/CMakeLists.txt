## TX-0 simulator
##
## This is an automagically generated file. Do NOT EDIT.
## Any changes you make will be overwritten!!
##
## Make changes to the SIMH top-level makefile and then run the
## "cmake/generate.py" script to regenerate these files.
##
##     cd cmake; python -m generate --help
##
## ------------------------------------------------------------

if (HAVE_UNITY_FRAMEWORK AND EXISTS "${CMAKE_CURRENT_SOURCE_DIR}/unit-tests/CMakeLists.txt")
  add_subdirectory(unit-tests)
endif ()

add_simulator(tx-0
    SOURCES
        tx0_cpu.c
        tx0_dpy.c
        tx0_stddev.c
        tx0_sys.c
        tx0_sys_orig.c
    INCLUDES
        ${CMAKE_CURRENT_SOURCE_DIR}
    FEATURE_VIDEO
    FEATURE_DISPLAY
    LABEL TX-0
    PKG_FAMILY default_family
    TEST tx-0)
