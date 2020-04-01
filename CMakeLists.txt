cmake_minimum_required(VERSION 3.14)

project(ImGui)

set(IMGUI_CORE_PATH ${PROJECT_SOURCE_DIR})

set(IMGUI_SOURCES
    ${IMGUI_CORE_PATH}/imconfig.h
    ${IMGUI_CORE_PATH}/imgui.h
    ${IMGUI_CORE_PATH}/imgui.cpp
    ${IMGUI_CORE_PATH}/imgui_draw.cpp
    ${IMGUI_CORE_PATH}/imgui_internal.h
    ${IMGUI_CORE_PATH}/imgui_widgets.cpp
    ${IMGUI_CORE_PATH}/imstb_rectpack.h
    ${IMGUI_CORE_PATH}/imstb_textedit.h
    ${IMGUI_CORE_PATH}/imstb_truetype.h
    ${IMGUI_CORE_PATH}/imgui_demo.cpp
)

add_library(ImGui STATIC ${IMGUI_SOURCES})
target_include_directories(ImGui PUBLIC ${IMGUI_CORE_PATH})