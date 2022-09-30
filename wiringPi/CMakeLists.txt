add_library(libwiringpi STATIC)

target_link_libraries(libwiringpi m pthread rt crypt)

set_property(TARGET libwiringpi PROPERTY C_STANDARD 99)
set_property(TARGET libwiringpi PROPERTY CXX_STANDARD 11)

target_sources(libwiringpi PUBLIC
        "${CMAKE_CURRENT_SOURCE_DIR}/wiringPi.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/wiringSerial.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/wiringShift.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/piHiPri.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/piThread.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/wiringPiSPI.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/wiringPiI2C.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/softPwm.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/softTone.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/mcp23008.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/mcp23016.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/mcp23017.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/mcp23s08.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/mcp23s17.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/sr595.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/pcf8574.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/pcf8591.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/mcp3002.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/mcp3004.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/mcp4802.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/mcp3422.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/max31855.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/max5322.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/ads1115.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/sn3218.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/bmp180.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/htu21d.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/ds18b20.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/rht03.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/drcSerial.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/drcNet.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/pseudoPins.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/wpiExtensions.c"
        )

target_include_directories(libwiringpi PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}")

