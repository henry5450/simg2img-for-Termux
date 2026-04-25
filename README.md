# simg2img-for-Termux
simg2img for Termux

Android simg2img (Termux Build)

A minimal build of simg2img that works in Android (Termux / aarch64).

Features
Works on Android (bionic libc)
No musl/glibc dependency issues
Built with clang (Termux)

Build:
 $ pkg install clang zlib
 $ clang++ -O2 -std=c++17 -o simg2img simg2img.cpp sparse.cpp sparse_crc32.cpp sparse_err.cpp sparse_read.cpp backed_block.cpp output_file.cpp android-base/stringprintf.cpp -Iinclude -Iandroid-base/include -lz
Usage:
./simg2img system.img system_raw.img

Notes
Built and tested on Termux (aarch64)
Should work on most Android devices
License

Same as AOSP (Apache 2.0)
