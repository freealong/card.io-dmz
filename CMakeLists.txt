set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -DCYTHON_DMZ -DSCAN_EXPIRY")

include_directories(${CMAKE_CURRENT_SOURCE_DIR})
include_directories("/usr/include/python2.7")

find_package(OpenCV 2)

set(SOURCE_FILES dmz_all.cpp)

add_library(dmz SHARED ${SOURCE_FILES})
target_link_libraries(dmz ${OpenCV_LIBRARIES})