<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

The DMA controller transfers data between a source and destination address without CPU intervention. It operates through multiple channels, handling read and write operations using AXI interfaces. Data is temporarily stored in a FIFO buffer, ensuring smooth transfer. The controller manages handshaking signals (READY/VALID) for efficient data flow and indicates completion with a done signal.

## How to test

Simulation: Use a Verilog testbench to provide input signals like trigger, source_address, destination_address, and length. Monitor the data transfer process and check the done signal.

Hardware Testing: Implement the design on an FPGA, provide memory-mapped addresses for data transfer, and verify successful data movement using debugging tools like SignalTap or ILA.

AXI Protocol Verification: Ensure correct read/write transactions by observing AR/AW/W/R/B handshake signals.

## External hardware

FPGA board (for hardware testing)

Memory (SRAM/DDR) or external peripherals (if required)

Debugging tools like JTAG, logic analyzers, or UART for status monitoring
