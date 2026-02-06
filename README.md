# Modern Synchronous FIFO (Verilog)

This repository contains a **modern, synthesizable synchronous FIFO** implemented in Verilog HDL and verified using **Xilinx Vivado Simulator**.  
The design follows industry-style coding practices and is suitable for academic projects, interviews, and real digital system applications.

---

## 📌 Features

- ✔ Parameterized **Data Width** and **Depth**
- ✔ Single-clock (synchronous) FIFO  
- ✔ Separate read and write pointers  
- ✔ Occupancy tracking using a counter  
- ✔ Status flags:
  - `empty`
  - `full`
  - `almost_empty`
  - `almost_full`
- ✔ Safe read/write (prevents overflow and underflow)
- ✔ Vivado-synthesizable and simulation-ready  
- ✔ Easy to extend for advanced systems  

---

## 📁 Files in this Repository

| File Name | Description |
|-----------|-------------|
| `modern_fifo.v` | Main FIFO module |
| `tb_modern_fifo.v` | Testbench for simulation |

---

## 🧠 How the FIFO Works (Brief)

- Data is written when `wr_en = 1` and FIFO is not full  
- Data is read when `rd_en = 1` and FIFO is not empty  
- Read and write pointers move circularly  
- A counter tracks how many elements are stored  
- Flags warn when FIFO is nearly full or empty  

This ensures **First-In, First-Out (FIFO)** behavior.

---

## 🚀 How to Run in Vivado

1. Open **Vivado → Create New Project**
2. Add these files:
   - `modern_fifo.v`
   - `tb_modern_fifo.v`
3. Set `tb_modern_fifo` as **top module**
4. Run **Simulation**
5. Open waveform and observe:
   - `wr_en`, `rd_en`
   - `wr_data`, `rd_data`
   - `empty`, `full`, `almost_full`, `almost_empty`

---

## 🛠 Applications

This FIFO can be used in:

- UART communication buffers  
- Image streaming systems  
- AI / IoT data pipelines  
- Network packet buffers  
- Real-time signal processing  
- Embedded systems  

---

## 📈 Future Improvements (Optional)

You can extend this design to:

- Dual-clock (Asynchronous) FIFO  
- AXI-Stream FIFO  
- FIFO with overflow/underflow protection  
- FIFO with handshake protocol  
- FIFO with reset recovery  

---

## 👤 Author

**Your Name**  
ECE Undergraduate | VLSI & Digital Design Enthusiast  

Feel free to fork, modify, and improve this design.

---

⭐ If you find this useful, give it a star!
