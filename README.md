# XDK2MAM is open source software to bridge the Bosch XDK110 and IOTA Tangle

The [Bosch XDK110](https://xdk.bosch-connectivity.com) is a programmable sensor device & a prototyping platform for many IoT use cases, being used in the field of Internet of Production, mainly to measure the performance of industrial machinery.

On the other side, IOTA's [Masked Authenticated Messaging (MAM)](https://blog.iota.org/introducing-masked-authenticated-messaging-e55c1822d50e) is a second layer data communication protocol which adds functionality to emit and access an encrypted data stream over the Tangle.

[XDK2MAM](https://xdk2mam.io) main goal is to provide open source software to allow interaction between this powerful hardware and the promising IOTA Tangle.

The following repository has either **C code** for the Bosch XDK110 and for the data receiver in **Node.js** where the attach to Tangle via MAM happens, featuring the different methods the XDK110 is capable of (HTTP/MQTT/BLE)

# This branch code has been tested in Workbench 3.6.0

While our goal is to always be up to the latest release of the [XDK Workbench](https://xdk.bosch-connectivity.com/software-downloads) (an Eclipse based IDE that comes with XDK to build software and flash it to the hardware), changes made by the Bosch team from release to release tend to leave our code with some compilation errors. 

This is an issue **we are reviewing actively with Bosch XDK team**. Until we sync we recommend to use our so called **CSVC** (current stable version to compile). This will allow you to build your project without errors so you can start working with your XDK inmmediatly after.

# How do you want to connect?

**This repository has packages for the XDK110 to stream its sensors data through:**

- **[HTTP](https://github.com/xdk2mam/xdk2mam/tree/Workbench-3.6/http-sdcard)** (WiFi on XDK will just post a request with the data to a given server)
- **[HTTP-SD Card](https://github.com/xdk2mam/xdk2mam/tree/Workbench-3.6/http-sdcard)** (same as HTTP but with a config file placed on the microSD card to allow portability)
- **[MQTT](https://github.com/xdk2mam/xdk2mam/tree/Workbench-3.6/mqtt)** (relay data to a MQTT Broker)
- **[BLE-SDCARD](https://github.com/xdk2mam/xdk2mam/tree/Workbench-3.6/ble-sdcard)** (send sensor's data from XDK110 to your Raspberry using Bluetooth Low Energy)
- **[DMP](https://github.com/xdk2mam/xdk2mam/tree/Workbench-3.6/dmp)** (our template to interact with the IOTA Data Marketplace)
- **[UDP](https://github.com/xdk2mam/xdk2mam/tree/Workbench-3.6/udp-sdcard)** (UDP method)
