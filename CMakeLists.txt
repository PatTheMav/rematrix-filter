cmake_minimum_required(VERSION 3.16)

project(rematrix-filter)

set(MACOSX_PLUGIN_GUI_IDENTIFIER "com.andersama.rematrix-filter")
set(MACOSX_PLUGIN_BUNDLE_VERSION "0.0.1")
set(MACOSX_PLUGIN_SHORT_VERSION_STRING "1")

find_package(libobs REQUIRED)
include(external/ObsPluginHelpers.cmake)

add_library(rematrix-filter MODULE)

target_sources(rematrix-filter
	PRIVATE rematrix-filter.cpp)

target_link_libraries(rematrix-filter
	PRIVATE OBS::libobs)

setup_plugin_target(rematrix-filter)
