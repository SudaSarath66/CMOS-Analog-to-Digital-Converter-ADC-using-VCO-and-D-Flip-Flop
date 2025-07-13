
# ⚡ CMOS Analog-to-Digital Converter (ADC) using VCO and D Flip-Flop in 90nm Technology

## 📌 Abstract

This project presents the design and simulation of a **CMOS Analog-to-Digital Converter (ADC)** based on a **Voltage-Controlled Oscillator (VCO)** and **D Flip-Flops (DFFs)** using **90nm technology** in **Cadence Virtuoso**. The analog signal is converted into a frequency-modulated output using a VCO, which is then sampled by edge-triggered DFFs to generate the digital output.

🧩 The architecture supports:
- ✅ High-speed operation  
- ✅ Low-power consumption  
- ✅ Compact layout for VLSI integration

---

## 🧱 Architecture Overview

The ADC consists of two fundamental blocks:

### 🔹 1. Voltage-to-Frequency Converter (VFC)
- Converts input analog voltage into frequency.
- Implemented using a **Voltage-Controlled Oscillator (VCO)**.
- Linearity and tuning range were optimized for 0.4V–1.0V inputs.

### 🔹 2. Frequency-to-Digital Converter (FDC)
- Samples frequency using **D Flip-Flops (DFFs)**.
- Converts frequency to digital codes.
- Reliable operation under corner cases.

> 🖇️ These two modules together form the complete ADC, converting analog inputs to digital outputs.

---

## 🧪 Simulation & Results

All blocks were designed and simulated in **Cadence Virtuoso** using 90nm CMOS PDK.

### 🔍 Simulation Scenarios

| Input Voltage (V) | Digital Output | Frequency Response | Power Trend |
|-------------------|----------------|--------------------|-------------|
| 0.4               | Low Code       | Low Frequency      | Low Power   |
| 0.6               | Mid Code       | Mid Frequency      | Medium      |
| 0.8               | High Code      | High Frequency     | Higher      |
| 1.0               | Max Code       | Max Frequency      | Highest     |

### 📈 Corner Analysis (Power Consumption)

| Process Corner | Power (µW)     |
|----------------|----------------|
| TT (Typical)   | 193.2          |
| FF (Fast)      | 275.8          |
| SS (Slow)      | 124.1 ✅        |
| FS (F-F / S-S) | 220 / 155.7    |

📌 **SS Corner** yields the best energy efficiency.
---

## 🚀 Features

- ✔️ Full-CMOS design at 90nm node  
- ✔️ Low-power, scalable architecture  
- ✔️ High-speed sampling using DFF  
- ✔️ Noise-tolerant VCO conversion  
- ✔️ Suitable for mixed-signal SoC, sensor front-ends, and biomedical ADCs.

