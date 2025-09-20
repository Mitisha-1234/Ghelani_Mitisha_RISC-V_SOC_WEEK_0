# Ghelani_Mitisha_RISC-V_SOC_WEEK_0
# RISC-V Reference SoC Tapeout Program VSD

<div align="center">

[![RISC-V](https://img.shields.io/badge/RISC--V-SoC%20Tapeout-blue?style=for-the-badge&logo=riscv)](https://riscv.org/)
[![VSD](https://img.shields.io/badge/VSD-Program-orange?style=for-the-badge)](https://vsdiat.vlsisystemdesign.com/)
![Participants](https://img.shields.io/badge/Participants-3500+-success?style=for-the-badge)
![India](https://img.shields.io/badge/Made%20in-India-saffron?style=for-the-badge)

</div>

# Project Description
This initiative introduces contributors to a full-stack open-source RTL-to-GDSII flow using the RISC-V processor architecture. It emphasizes hands-on VLSI design, simulation, and digital layout using commonly used FOSS tools suited for academic and hobbyist SoC development.

# Learning Components:
RISC-V architectural basics and open-source IP cores
Practice with RTL coding, simulation, and waveform analysis
Synthesis and netlist preparation with Yosys
Integrating open-source EDA workflows from initial code to the creation of GDSII layout files

# Importance:
Engagement in this project helps participants build practical chip-design skills, fosters a vibrant community, and supports the expanding reach of domestic and global open-silicon efforts.


### ⚙️ System Requirements
| Resource | Requirement |
|----------|-------------|
| RAM      | 6 GB |
| Storage  | 50 GB HDD |
| OS       | Ubuntu 24.04.3 |
| CPU      | 4 vCPU |
Each tool below is required for a different stage of the RTL-to-GDS flow, making the setup essential.

#### <ins>**Yosys**</ins>
Translates Verilog files into optimized logic networks; forms the starting point for most digital backend design flows.
```
$ sudo apt-get update
$ sudo apt install git                 
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys
$ git submodule update --init --recursive
$ sudo apt install make               # If make is not installed
$ sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
$ make
$ sudo make install
```
```
$ yosys
```
A successful installation produces a Yosys shell prompt, confirming the tool is ready for use.
![Yosys](https://github.com/user-attachments/assets/4e21dd04-9b85-4529-938b-99bbfee4e5fd)

#### <ins>**Iverilog - Verilog Simulator (Testbench & Logic Verification**</ins>
Run Verilog simulation to verify RTL logic matches design intent before synthesis.
```
sudo apt-get update
sudo apt-get install iverilog
iverilog -v
```
Installation output and version checks confirm Icarus Verilog is correctly set up for running your simulations.

![IVerilog ](https://github.com/user-attachments/assets/a6d15dba-74ae-4416-af24-5d5d7d7516d1)

#### <ins>**GTKWave - Signal Viewer for Digital Simulation**</ins>
Helps in opening VCD/FSDB waveform files to interactively inspect simulation results and debug logic bugs.
```
$ sudo apt-get update
$ sudo apt install gtkwave
```
View simulation output graphically and cross-check signal transitions to ensure correct design behavior.
![GTK Wave](https://github.com/user-attachments/assets/9ba75b3d-6cfc-41a9-9770-a3f6490c0734)





