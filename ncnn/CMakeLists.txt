AUX_SOURCE_DIRECTORY(./ SRC_FILES)
set(DEMO_NAME ntnn)

find_package(ncnn)
include_directories(${NCNN_DIR}/include)

add_executable(${DEMO_NAME} ${SRC_FILES})

target_link_libraries(${DEMO_NAME} ${OpenCV_LIBS} ${Caffe_LIBRARIES} ncnn)
