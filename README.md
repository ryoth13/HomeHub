# HomeHub

家庭智能设备中枢控制系统。

HomeHub 是一个基于 STM32F411CEU6 的模块化家庭智能设备中枢控制系统。

项目以 STM32F411CEU6 作为核心 MCU，运行 FreeRTOS，使用 LVGL 构建图形用户界面，并通过 ESP-01S 提供 Wi-Fi 网络连接能力。

系统计划与基于 OpenWrt 的家庭路由器进行通信，用于获取家庭网络及 Wi-Fi 相关信息。

Wi-Fi 信息查看只是 HomeHub 的其中一个功能，项目最终目标是构建一个可持续扩展的家庭智能设备中枢平台。


## Hardware

| Hardware | Description |
| --- | --- |
| STM32F411CEU6 | Core MCU |
| ESP-01S | Wi-Fi communication module |
| ILI934V | 2.8-inch SPI LCD |
| Touch Panel | SPI touch input |
| W25Q64 | External SPI Flash |


## Software Stack

| Category | Technology |
| --- | --- |
| MCU | STM32F411CEU6 |
| CPU | ARM Cortex-M4F |
| RTOS | FreeRTOS |
| GUI | LVGL |
| Wi-Fi | ESP-01S / ESP8266 |
| Router | OpenWrt |
| Language | C |
| Compiler | ARM GNU Toolchain |
| Build System | CMake |
| Build Tool | Ninja |
| Debugger | J-Link |
| Debug Interface | SWD |
| Host OS | macOS |
| Version Control | Git / GitHub |


## Architecture

项目采用模块化设计。

```text
Application
     │
     ▼
 Services
     │
     ▼
 Devices
     │
     ▼
 Drivers
     │
     ▼
 STM32 HAL / CMSIS
     │
     ▼
 STM32F411CEU6

FreeRTOS 负责系统任务、队列、同步以及事件管理。

LVGL 负责图形用户界面。

ESP-01S 负责 Wi-Fi 网络连接。

OpenWrt 作为家庭网络侧的信息来源。

Planned Features
 System status
 Wi-Fi information
 Network information
 OpenWrt information
 LAN device information
 Device management
 Configuration management
 Logging system
 W25Q64 storage
 MQTT
 Smart home device integration
Development

开发环境：

macOS
ARM GNU Toolchain
CMake
Ninja
J-Link
Git
Project Status

🚧 Under Development

当前项目处于初始化阶段。

硬件、软件架构以及具体模块将随着开发逐步完善。

License

TBD
