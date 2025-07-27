# CMOS-Aware Power & Delay Estimator with Technology Node Scaling 🧠🔬

A Python-based analytical tool to estimate **gate delay**, **dynamic power**, and **static power** for standard CMOS logic gates, with **technology node scaling** from 180nm to 7nm.

---

## 📘 Abstract

This project aims to model and visualize the delay and power consumption in CMOS logic gates across different technology nodes. As technology scales down (e.g., from 180nm to 7nm), power density and performance vary significantly. This estimator provides a simplified but effective Python-based tool for students and professionals to analyze and compare CMOS gate performance using well-known equations.

---

## 🧮 Equations & Theory

### 1. **Gate Delay**  
\[
{Delay} = 0.69 \times R \times C
\]

- **R**: Equivalent resistance of the transistor (from tech node)
- **C**: Load capacitance (from gate/load)

---

### 2. **Dynamic Power**  
\[
P_{dynamic} = \alpha \times C \times V_{dd}^2 \times f
\]

- **α**: Switching activity factor (typically 0.1–1)
- **C**: Load capacitance
- **Vdd**: Supply voltage
- **f**: Clock frequency

---

### 3. **Static Power**  
\[
P_{static} = I_{leak} \times V_{dd}
\]

- **I_leak**: Leakage current
- **Vdd**: Supply voltage

These equations reflect first-order CMOS models suitable for education and preliminary estimation.

---

## 🖼️ Screenshots

### Sample Input & Output
![Terminal Output](<img width="392" height="189" alt="Screenshot 2025-07-27 220401" src="https://github.com/user-attachments/assets/69e5eb88-571a-4816-97cb-2d8f813f72a7" />
)

---

## 📈 Graphs

### Delay vs Technology Node
![Delay Graph](<img width="790" height="493" alt="Screenshot 2025-07-27 220419" src="https://github.com/user-attachments/assets/754aaa3c-ba4d-4546-9762-6c4357d59d42" />
)

### Dynamic & Static Power vs Node
![Power Graph](<img width="787" height="493" alt="Screenshot 2025-07-27 220435" src="https://github.com/user-attachments/assets/91acee63-d7c7-42f1-a42c-58a73f7edd48" />
)

Graphs generated using `matplotlib` — auto-scaled for clarity and insight.

---

## 💻 Code Explanation

### 🔹 `main.py`  
Handles user input (gate type, node, frequency), calls the estimator functions, and prints results.

### 🔹 `tech_nodes.py`  
Contains dictionaries of R, C, Vdd, and I_leak values for different technology nodes.

### 🔹 `gates.json`  
Defines basic CMOS gates like NAND, NOR, INV with switching activity and load values.

### 🔹 `graph_plotter.py`  
Plots delay and power across nodes using `matplotlib`.

### 🔹 `CMOS_Estimator_Report.docx`  
A 10-page academic-style project report covering theory, equations, screenshots, and analysis.

---

## 📊 Sample Output

```bash
Gate: NAND2
Node: 45nm
Frequency: 500 Hz

Delay: 1.8630e-12 s
Dynamic Power: 2.4000e-13 W
Static Power: 3.2000e+01 W
