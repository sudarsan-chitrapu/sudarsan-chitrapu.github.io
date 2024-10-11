---
title: "Dynamic partial reconfiguration of an image processing sensor node"
excerpt: "In this project, we built a dynamically partially reconfigarable image processing sensor node using zynq-2000<br/><img src='/images/reconfig.png'>"
collection: portfolio
---

In this project, we implementd a remote complete reconfiguration of a zed-board-based sensor node with the help of the ZigBee communication interface. One of the key highlights of this project would be avoiding the use of any external/internal IP as a controller for reconfiguration. This reduces significant power consumption and gives more space for application logic, both of which are key requirements of a sensor node. The system has to have two main functionalities to enable remote reconfiguration:
1. Wireless access to flash memory on the FPGA to upload new configuration bitstream
2. Mechanism to remotely trigger the FPGA to reload the new configuration bitstream

To gain access to flash memory, a ZigBee module was be used. This requires the UART controller
and SPI controller logic blocks for providing connections to the Zigbee module and flash memory
respectively. We used the ICAP primitive of the zed board that allows control of built-in configuration logic.

[Click here to view the source code](https://github.com/sudarsan-chitrapu/Reconfigurable-FPGA-Sensor-Node)
