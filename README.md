# bgfx.cmake

This repo contains a bunch of cmake files that can be used to build bgfx with CMake.

## Building

```bash
git clone --recurse-submodules https://github.com/openblack/bgfx.cmake.git
cd bgfx.cmake
cmake -B build
```

# How To Use

You can either use bgfx.cmake to create an install target or include it directly in your CMake project.

## Install Target

You can build an install target using CMake consisting of binaries that can be added using find_package in your projects.

```bash
cmake -B build -DCMAKE_INSTALL_PREFIX=./install -DCMAKE_DEBUG_POSTFIX=d -DBGFX_BUILD_EXAMPLES=OFF -DBGFX_BUILD_TOOLS=ON -DBGFX_INSTALL=ON
cmake --build build --target install --config Debug
cmake --build build --target install --config Release
```

## Include in your project

This repo can be included in your own project directly through CMake, this is useful for development:

```cmake
add_subdirectory(bgfx.cmake)
```