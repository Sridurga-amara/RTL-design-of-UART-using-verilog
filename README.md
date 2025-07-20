# UART Communication System using Verilog

This project implements a complete **UART (Universal Asynchronous Receiver/Transmitter)** communication system using Verilog HDL.  
It includes the design of a baud rate generator, a UART transmitter, a receiver, and a testbench for simulation.

---

## 📌 Project Highlights

- **Language**: Verilog HDL  
- **Simulation Tool**: Xilinx Vivado  
- **Modules Included**:
  - Baud Rate Generator  
  - UART Transmitter  
  - UART Receiver  
  - Testbench  
- **Baud Rate**: 9600 bps  
- **Clock Frequency**: 50 MHz  

---

## ⚙️ Functional Overview

UART is a widely used asynchronous serial communication protocol.  
This design enables full-duplex communication between devices using only two lines: **TX** (transmit) and **RX** (receive).

- **Baudrate Module**: Generates baud ticks based on the target baud rate.  
- **UART_TX Module**: Converts parallel 8-bit data into a serial stream with start, data, and stop bits.  
- **UART_RX Module**: Detects the incoming serial bits and reconstructs them into parallel data.  

---

## ✅ Advantages of UART

- Reduces error by up to ~30–50% in noisy environments compared to SPI/I2C due to start/stop bit synchronization  
- Built-in framing and optional parity allow simple error detection  
- Supports longer distances without additional hardware  
- Easier to debug due to visible bit-level framing  

---

## 🚀 Performance & Speed

While UART operates slower than SPI in raw speed, it offers **better reliability** for medium-speed applications.  
Compared to I2C:

- UART typically achieves **~40% faster data transfer** at similar hardware cost and complexity  
- Less prone to **bus contention** and **clock stretching issues** seen in I2C  

---

## 🧪 Simulation Result (From Testbench)

- Transmission of 8-bit binary: `11110000`  
- Observed proper start bit, data bits, and stop bit on TX line  
- Data successfully received and validated on RX side with `rx_done` asserted  

---

## 💡 Applications

- Serial data logging or debugging  
- Interfacing microcontrollers with Bluetooth/GSM/GPS modules  
- Low-pin communication between FPGA and sensors  
- Real-time monitoring systems  

---

## 🛠 Future Improvements

- Add parity bit support for stronger error detection  
- Implement configurable baud rate  
- Include FIFO buffering for burst data transfer  
