# jemalloc

?: -DJEMALLOC_C11ATOMICS:BOOL=OFF

# re2: RE2_BUILD_TESTING=OFF

R:\tf\tensorflow\contrib\cmake\external\re2.cmake
append: after L43:      -DRE2_BUILD_TESTING:BOOL=OFF

# C / CXX Host: X64

```
C:\Program Files\CMake\share\cmake-3.9\Modules\CMakeCXXCompiler.cmake.in
replace: @CMAKE_CXX_COMPILER@ => D:/Program Files/Microsoft Visual Studio/2017/Community/VC/Tools/MSVC/14.11.25503/bin/HostX64/x64/cl.exe
replace: @CMAKE_LINKER@ => D:/Program Files/Microsoft Visual Studio/2017/Community/VC/Tools/MSVC/14.11.25503/bin/HostX64/x64/link.exe

C:\Program Files\CMake\share\cmake-3.9\Modules\CMakeCCompiler.cmake.in
replace: @CMAKE_CXX_COMPILER@ => D:/Program Files/Microsoft Visual Studio/2017/Community/VC/Tools/MSVC/14.11.25503/bin/HostX64/x64/cl.exe
replace: @CMAKE_LINKER@ => D:/Program Files/Microsoft Visual Studio/2017/Community/VC/Tools/MSVC/14.11.25503/bin/HostX64/x64/link.exe
```

But the action above is useless - must `mv HostX86{,.old}` and `ln -s HostX64 HostX86`

# Delete broken tensorflow_WIN_CPU_SIMD_OPTIONS
R:\tf\tensorflow\contrib\cmake\CMakeLists.txt
replace: L34 => set(tensorflow_WIN_CPU_SIMD_OPTIONS "${tensorflow_WIN_CPU_SIMD_OPTIONS}")

# Use Custom CMakeCache.txt

# Download files (needed in China):
download manually
* https://storage.googleapis.com/libpng-public-archive/libpng-1.2.53.tar.gz

and then copy to the download folder
