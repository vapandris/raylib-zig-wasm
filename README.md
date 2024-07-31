# raylib-zig-wasm
A really simple example and a guide on how to make raylib-zig work with wasm

Zig version is 0.12 for stability

## Dependencies:
- zig version 0.12: https://ziglang.org/
- raylib-zig (branch 0.12): https://github.com/Not-Nik/raylib-zig/tree/zig-0.12
- emsdk: https://emscripten.org/
- python 3.6 (or newer)

## Steps to take for wasm compilation:
- make sure that the hash is correct in build.zig.zon (can check with zig build)
- run: zig build -Dtarget=wasm32-emscripten --sysroot \<emsdk-location\>/upstream/emscripten
- can check output in: zig-out/htmlout/
- start localhost server with: python -m https.server
- open http://localhost:8000/
- open zig-out/htmlout/ & profit
