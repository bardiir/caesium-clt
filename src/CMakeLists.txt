set(CMAKE_C_FLAGS "--std=gnu99")

FILE(GLOB CSources *.c)
FILE(GLOB CHeaders *.h)

add_executable(caesiumclt ${CSources} ${CHeaders})

target_link_libraries(caesiumclt LINK_PUBLIC caesium)
target_link_libraries(caesiumclt LINK_PUBLIC m)

install(TARGETS caesiumclt DESTINATION bin)