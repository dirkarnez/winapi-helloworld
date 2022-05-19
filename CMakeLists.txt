cmake_minimum_required(VERSION 3.8)
project(winapi-helloworld)


SET(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -static -Wl,--subsystem,windows")

add_executable(${PROJECT_NAME} WIN32 
    "src/main.cpp"
)

target_compile_definitions(${PROJECT_NAME} PRIVATE _UNICODE UNICODE)
