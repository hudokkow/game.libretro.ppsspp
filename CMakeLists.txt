cmake_minimum_required(VERSION 3.1)
project(game.libretro.ppsspp)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-ppsspp REQUIRED)

set(DEPLIBS ppsspp)
set(PPSSPP_CUSTOM_BINARY ${PPSSPP_LIB}
                         ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} PPSSPP DEPLIBS)
