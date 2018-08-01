# atomicIncTest

Simple project to test the use of atomicInc and atomicDec

## Usage

### Linux
```
./bin/release/atomicIncTest <repeats> <iterations> <threads> <device_id>
```
with values

i.e. `./bin/release/atomicIncTest 4 16 65536 0 0`


## Building using CMake

To build using cmake it is recommended to use out of source building. i.e. 


    mkdir build 
    cd build
    cmake ..
    make

To create a debug build, use -D

    mkdir debug 
    cd debug
    cmake .. -DCMAKE_BUILD_TYPE=Debug
    make

To create a profile build, use -D

    mkdir profile 
    cd profile
    cmake .. -DCMAKE_BUILD_TYPE=Profile
    make

To target specific CUDA architectures, specify a semicolon separated list: ie.

    mkdir build 
    cd build
    cmake .. -DSMS="52;60"
    make


