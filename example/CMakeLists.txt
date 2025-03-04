cmake_minimum_required(VERSION 3.25)
project(fortran-towboat Fortran)

enable_language(Fortran)

set(SRC_DIR ${CMAKE_SOURCE_DIR}/app)
set(SRC_FILES ${SRC_DIR}/main.f90)

add_executable(fortran-towboat ${SRC_FILES})

add_custom_target(run
    COMMAND fortran-towboat
    DEPENDS fortran-towboat
    WORKING_DIRECTORY ${CMAKE_BINARY_DIR}
)