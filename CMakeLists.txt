#project_name is your project name
PROJECT(project_name)

CMAKE_MINIMUM_REQUIRED(VERSION 2.6)
if(COMMAND cmake_policy)
      cmake_policy(SET CMP0003 NEW)
endif(COMMAND cmake_policy)

FIND_PACKAGE( OpenCV REQUIRED )

# Declare the target (an executable)
# minarea.c is your c file for compire
ADD_EXECUTABLE(project_name  minarea.c)

TARGET_LINK_LIBRARIES(project_name ${OpenCV_LIBS})

#MESSAGE(STATUS "OpenCV_LIBS: ${OpenCV_LIBS}")
