cmake_minimum_required(VERSION 2.8)
project( Color_Segmentador_Trainer)

find_package( OpenCV REQUIRED )



set(CUDA_USE_STATIC_CUDA_RUNTIME OFF)

set(HEADERS
   ${HEADERS}
   ${CMAKE_CURRENT_SOURCE_DIR}/Segmenter.h

)

add_executable( color_segmentador mainSegmentador.cpp )
target_link_libraries( color_segmentador ${OpenCV_LIBS})
