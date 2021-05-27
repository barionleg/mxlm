# cmake for mxml
#
# template from https://dominikberner.ch/cmake-interface-lib/
#

cmake_minimum_required(VERSION 3.12)

project("mxml"
        VERSION 1
        DESCRIPTION "XML encoder and decoder for use with MIDAS"
        HOMEPAGE_URL "https://midas.triumf.ca")

add_library(${PROJECT_NAME} INTERFACE)

target_include_directories(${PROJECT_NAME} INTERFACE
   $<BUILD_INTERFACE:${${PROJECT_NAME}_SOURCE_DIR}>
   $<INSTALL_INTERFACE:${CMAKE_INSTALL_INCLUDEDIR}>)
   
#target_include_directories(${PROJECT_NAME} INTERFACE .)

target_compile_features(${PROJECT_NAME} INTERFACE cxx_std_11)

# end
