# TinyML-face-recognition-on-STM32F411RE-
TinyML face-recognition on STM32F411RE — INT8 quantized CNN deployed with STM32Cube.AI. Serial UART output for inference results.

# TinyFace-Stm32F411RE

TinyML face-recognition on the NUCLEO-F411RE (STM32F411RE) using an INT8 quantized CNN exported with TensorFlow Lite and deployed with **STM32Cube.AI**.

**What this repo contains**
- `Core/`, `Drivers/` etc. — STM32CubeIDE project files (generated).
- `network*` — Cube.AI generated model code (`network.c`, `network.h`, `network_data.c`, ...).
- `img.h` / `img.c` — Test image arrays (INT8) used as input on MCU.
- `README.md` — this file.
  

---

## Features
- INT8 quantized CNN (5-class face recognition).
- Runs fully offline on STM32F411RE (Cortex-M4).
- UART serial output showing predicted class and score.
- Simple example to test and extend with your own images.

---

## Quick start (flash & run)
1. Open the project in **STM32CubeIDE**.
2. Build the project (`Project → Build All`).
3. Flash to the board (`Run → Debug` or use ST-Link / STM32CubeProgrammer`).
4. Open Serial Terminal at **115200 8N1** (e.g. PuTTY, Tera Term, minicom).
5. Reset the board — you should see:

