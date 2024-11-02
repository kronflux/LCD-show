cmake_minimum_required(VERSION 2.8)

SET(COMPILE_DEFINITIONS -Werror)

include_directories(/usr/include/vc/include)
include_directories(/usr/include/interface/vcos/pthreads)
include_directories(/usr/include/interface/vmcs_host)
include_directories(/usr/include/interface/vmcs_host/linux)

add_executable(fbcp main.c)

target_link_libraries(fbcp bcm_host)
