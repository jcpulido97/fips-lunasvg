#
# project: fips-lunasvg
#
if (NOT FIPS_IMPORT)
    cmake_minimum_required(VERSION 3.11)
    project(fips-lunasvg)
    # include the fips main cmake file
    get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
    include("${FIPS_ROOT_DIR}/cmake/fips.cmake")
    fips_setup()
endif()

fips_begin_module(lunasvg)
fips_end_module()

add_subdirectory(lunasvg/include)
add_subdirectory(lunasvg/source)
add_subdirectory(lunasvg/3rdparty/software)
add_subdirectory(lunasvg/3rdparty/plutovg)

if (NOT FIPS_IMPORT)
    fips_finish()
endif()
