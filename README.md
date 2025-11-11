# Shadow Node

Credit-card sized pocket supercomputer for AR glasses (PiercePrism v3).

## Day 1 (Nov 11, 2025)
- Full software stack ready  
- Custom OS image (QEMU tested)  
- ESP32-S3 clip firmware compiled  
- 60 FPS wireless desktop streaming working in simulation  

Hardware (Pi Zero 2 W) arrives tomorrow → unboxing + prism demo.

## Quick Start (QEMU on Windows)
```bat
curl -L -o Shadow-Node-v0.1.img.xz https://tinyurl.com/shadow-v01-img  (hosted shortly)
7z x Shadow-Node-v0.1.img.xz
qemu-system-aarch64 -M raspi3b -cpu cortex-a72 -m 1024 -smp 4 -drive file=Shadow-Node-v0.1.img,format=raw -net nic -net user,hostfwd=tcp::5900-:5900,hostfwd=tcp::22-:22 -nographic

Login: pi / shadow2025VNC: localhost:5900

