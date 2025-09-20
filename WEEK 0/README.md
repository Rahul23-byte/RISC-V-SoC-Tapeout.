# 🚀 Week 0 – Kickoff: VLSI System Design (VSD) Journey & Toolchain Setup  

This marks the **beginning of my VLSI System Design (VSD) Program journey**. The very first milestone was to **build a strong foundation by setting up the working environment** — ensuring that all the necessary open-source tools for synthesis, simulation, circuit analysis, and layout are ready to go.  

The objective of this week was clear:  
👉 **Create a stable, resource-optimized workspace** for smooth execution of RTL design, verification, and analysis tasks.  

---

## 🖥️ Virtual Machine Setup – My Workstation Blueprint  

To balance efficiency with performance, I deployed a **Virtual Machine (VM)** tailored for VLSI workflows. 

<div align="center">

| **Specification 💻** | **Details 📋** |  
|-----------------------|----------------|  
| **OS 🐧** | Ubuntu 20.04 (or higher) |  
| **RAM 💾** | 6 GB |  
| **Storage 💿** | 50 GB HDD |  
| **vCPUs ⚡** | 4 cores |  

</div>

💡 *Insight:* With this configuration, even complex synthesis and simulation workloads can be handled without hiccups.  

---

## ⚙️ Open-Source Toolchain – Installed & Verified  

A complete VLSI flow requires different tools at different design stages. This week, I ensured each one was installed, tested, and ready for action.  

### 🔧 Tools in the Flow  
1. **Yosys** 🧠 – *RTL Synthesis Engine*  
   - Function: Translates RTL code into a gate-level netlist.  

2. **Icarus Verilog (Iverilog)** 📟 – *Simulation Platform*  
   - Function: Compiles & simulates Verilog designs.  

3. **GTKWave** 📊 – *Waveform Visualizer*  
   - Function: Provides an intuitive GUI to analyze simulation results.  

4. **Ngspice** ⚡ – *Circuit-Level Simulation*  
   - Function: Handles analog and mixed-signal circuit simulations.  

5. **Magic VLSI** 🎨 – *Layout Tool*  
   - Function: Enables physical design and layout visualization.  

✅ *Each tool was installed and successfully verified using test commands.*  

---


## ✅ **Yosys Installation**

```bash
# Day 0 - Tools Installation
## Yosys

$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys 
$ sudo apt install make # (If make is not installed please install it) 
$ sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make 
$ sudo make install
```

## 📷 **Installation Verification**
<p align="center">
  <img src="https://github.com/Rahul23-byte/RISC-V-SoC-Tapeout./blob/main/WEEK%200/yosys.png" 
       alt="Yosys Installed" width="600"/>
</p>

<div align="center">

✅ **Yosys Successfully Installed**

</div>

---

### 📟 **2. Iverilog – Verilog Simulator**

<details>
<summary><b>Purpose:</b> Compiles and simulates Verilog designs for functional verification.</summary>

Icarus Verilog is a Verilog simulation and synthesis tool that supports the IEEE-1364 Verilog HDL standard.

</details>

## **Iverilog Installation**
```bash
$ sudo apt-get install iverilog
```

## 📷 **Installation Verification**
<p align="center">
  <img src="https://github.com/Rahul23-byte/RISC-V-SoC-Tapeout./blob/main/WEEK%200/iverilog.png" 
       alt="Iverilog Installed" width="600"/>
</p>

<div align="center">

✅ **Iverilog Successfully Installed**

</div>

---

### 📊 **3. GTKWave – Waveform Viewer**

<details>
<summary><b>Purpose:</b> Analyzes and visualizes simulation waveforms for debugging.</summary>

GTKWave is a fully featured GTK+ based wave viewer for Unix, Win32, and Mac OSX.

</details>

## **GTKWave Installation**
```bash
$ sudo apt update
$ sudo apt install gtkwave
```

## 📷 **Installation Verification**
<p align="center">
  <img src="https://github.com/Rahul23-byte/RISC-V-SoC-Tapeout./blob/main/WEEK%200/GTKWave.png " 
       alt="GTKWave Installed" width="600"/>
</p>

<div align="center">

✅ **GTKWave Successfully Installed**

</div>

---

### ⚡ **4. Ngspice – Circuit Simulator**

<details>
<summary><b>Purpose:</b> Performs analog and mixed-signal circuit simulation.</summary>

Ngspice is a mixed-level/mixed-signal circuit simulator based on Spice3f5, Cider1b1 and Xspice.

</details>

## **Ngspice Installation**
```bash
$ sudo apt update
$ sudo apt install ngspice
```

## 📷 **Installation Verification**
<p align="center">
  <img src="https://github.com/Rahul23-byte/RISC-V-SoC-Tapeout./blob/main/WEEK%200/ngspice.png" 
       alt="ngspice Installed" width="600"/>
</p>

<div align="center">

✅ **Ngspice Successfully Installed**

</div>

---

### 🎨 **5. Magic VLSI – Layout Tool**

<details>
<summary><b>Purpose:</b> Creates, edits, and analyzes VLSI layouts with DRC capabilities.</summary>

Magic VLSI is an open-source VLSI layout tool widely used for IC design, DRC, and visualization.

</details>

## ✅ **Magic VLSI Installation**

[Magic VLSI](http://opencircuitdesign.com/magic/) is an open-source VLSI layout tool widely used for IC design, DRC, and visualization.  

Follow the steps below to install Magic on an Ubuntu/Debian system:

```bash
# Install required dependencies
sudo apt-get install m4
sudo apt-get install tcsh
sudo apt-get install csh
sudo apt-get install libx11-dev
sudo apt-get install tcl-dev tk-dev
sudo apt-get install libcairo2-dev
sudo apt-get install mesa-common-dev libglu1-mesa-dev
sudo apt-get install libncurses-dev

# Clone Magic repository
git clone https://github.com/RTimothyEdwards/magic
cd magic

# Configure build
./configure

# Build Magic
make

# Install system-wide
sudo make install
```

## 📷 **Installation Verification**
<p align="center">
  <img src="https://github.com/Rahul23-byte/RISC-V-SoC-Tapeout./blob/main/WEEK%200/Magic%20VLSI.png" 
       alt="magic vlsi Installed" width="600"/>
</p>

<div align="center">

✅ **Magic VLSI Successfully Installed**

</div>

---

<div align="center">

# 🎉 Installation Recap – Week 0  

All the essential tools are now up and running, forming a **complete open-source VLSI toolchain**. This setup ensures readiness for everything from RTL coding to physical design.  

---

## 📦 Installed Tools & Status  

| **Tool 🔧** | **Status ✅** | **Primary Role 🎯** |  
|-------------|---------------|---------------------|  
| 🧠 **Yosys** | ✅ Complete | RTL Synthesis → Gate-level Netlist |  
| 📟 **Icarus Verilog (Iverilog)** | ✅ Complete | Verilog Compilation & Simulation |  
| 📊 **GTKWave** | ✅ Complete | Waveform Viewing & Analysis |  
| ⚡ **Ngspice** | ✅ Complete | Circuit & Mixed-Signal Simulation |  
| 🎨 **Magic VLSI** | ✅ Complete | Layout Design & Visualization |  

✨ **Environment Ready →** Smooth VLSI design workflow from *RTL → GDS*!  

---

## 🌟 Key Takeaways  
<div align="left">


- ✅ A fully functional VM environment tailored for VLSI workflows is live.  
- 🔧 Each open-source EDA tool has been installed and verified.  
- 📈 The toolchain covers the entire digital design flow — from synthesis to layout.  
- 🚀 The setup forms the foundation for upcoming RTL, verification, and layout tasks in the VSD journey.  

</div>

---

## 📂 Project Metadata  

<div align="left">
   
- 📂 **Repository**: [RISC-V-SoC-Tapeout.](  )   
- 👨‍💻 **Author**: [Rahul23-byte] ()
- 📚 **Program**: *VLSI System Design (VSD)*  

</div>
---
