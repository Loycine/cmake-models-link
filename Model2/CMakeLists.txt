CMAKE_MINIMUM_REQUIRED(VERSION 3.0)
SET_PROPERTY(GLOBAL PROPERTY USE_FOLDERS On)

PROJECT (Model2)

SET(CMAKE_BUILD_TYPE Release)

INCLUDE_DIRECTORIES(.)

FILE(GLOB SOURCES "./*.cpp")

SET(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)           
SET(CMAKE_ARCHIVE_OUTPUT_DIRECTORY_DEBUG ${PROJECT_SOURCE_DIR}/lib) 
SET(CMAKE_ARCHIVE_OUTPUT_DIRECTORY_RELEASE ${PROJECT_SOURCE_DIR}/lib) 

ADD_LIBRARY(Model2 STATIC ${SOURCES})
SET_TARGET_PROPERTIES(${prj_target} PROPERTIES FOLDER "test") 