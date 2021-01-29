cmake_minimum_required(VERSION 3.9)
project(glad)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)

add_library(${PROJECT_NAME} src/glad.c)


set(CMAKE_INSTALL_PREFIX /usr/local/)

install(TARGETS ${PROJECT_NAME}
        DESTINATION ${CMAKE_INSTALL_PREFIX}/lib)

set(HEAD_FILES ${CMAKE_CURRENT_SOURCE_DIR}/include/)

install(DIRECTORY ${HEAD_FILES}
        DESTINATION ${CMAKE_INSTALL_PREFIX}/include)

#uinstall 
include(gladuninstall.cmake)