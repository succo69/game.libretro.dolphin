cmake_minimum_required(VERSION 3.1)
project(game.libretro.dolphin)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-dolphin REQUIRED)

set(DOLPHIN_CUSTOM_BINARY ${DOLPHIN_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} DOLPHIN "")

include(CPack)
