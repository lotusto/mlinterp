PROJECT(MULTILINEAR_INTERPOLATION)
CMAKE_MINIMUM_REQUIRED(VERSION 2.8.2)

# Install
SET(CMAKE_SKIP_INSTALL_ALL_DEPENDENCY true)
INSTALL(FILES ${PROJECT_SOURCE_DIR}/mlinterp/mlinterp ${PROJECT_SOURCE_DIR}/mlinterp/mlinterp.hpp DESTINATION include)

# C++11
SET(CMAKE_CXX_STANDARD 11)

# Module path
SET(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

# mlinterp
INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/mlinterp)

# Set appropriate optimization flags
# For debugging, use `cmake -DCMAKE_BUILD_TYPE=Debug .`
SET(CMAKE_BUILD_TYPE Release)

# Where to output binaries
SET(PROJECT_BINARY_DIR ${PROJECT_SOURCE_DIR}/bin)
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR})
ADD_SUBDIRECTORY(examples)

