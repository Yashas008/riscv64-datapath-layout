# riscv64-datapath-layout
 Analog custom layout of a 64-bit RISC-V datapath using Cadence Virtuoso
# RISC-V 64-Bit Datapath – Full-Custom Analog Layout (GPDK090)

This repository contains the    GDSII layout files    for selected full-custom standard cells designed using    Cadence Virtuoso IC615    with the    GPDK090 90nm CMOS process   . These cells will be used as part of a larger effort to construct a custom    64-bit RISC-V datapath   , including logic blocks such as ALUs, registers, and control logic.

All cells are verified using    Assura DRC and LVS   , and exported as clean GDSII files viewable using KLayout or other tools.



   🧠 Project Goals

- Create a full-custom analog layout of fundamental logic blocks.
- Build up from    basic gates    (Inverter, NOR) to complex datapath components.
- Verify all cells through    DRC    and    LVS   .
- Simulate pre/post-layout designs using    HSPICE or Spectre   .
- Export clean    GDSII    layout for documentation and hierarchical integration.



   📁 Directory Structure

| Folder         | Description |
|----------------|-------------|
| `gds/`         | Final GDSII files exported from Virtuoso layout view |
| `screenshots/` | Layout screenshots (optional, for report/presentation) |
| `README.md`    | This project summary |
| `.gitignore`   | Filters out irrelevant files (sim data, logs, etc.) |



   🧩 Cells Included

  # ✅ Inverter (INV)

-    Function   : Logic inversion
-    DRC   : Clean (Assura)
-    LVS   : Matched
-    Notes   :
  - PMOS enclosed in N-well
  - Proper P+ and N+ taps used
  - Clean layout with single VDD/VSS rail

  # ✅ 2-input NOR Gate

-    Function   : Logic NOR (universal gate)
-    DRC   : Clean (Assura)
-    LVS   : Matched
-    Notes   :
  - Series NMOS, parallel PMOS stack
  - Verified well spacing and contact placement
  - Fully functional for logic-level simulation



   🔧 Tools & Environment

| Tool            | Version / Notes |
|-----------------|-----------------|
| Cadence Virtuoso | IC6.1.5 (32-bit) |
| Assura DRC & LVS | For rule checking and netlist verification |
| GPDK090 PDK      | Generic 90nm CMOS process |
| KLayout          | For GDSII viewing |
| HSPICE / Spectre | (Future: for simulation) |



   ✅ Verification Summary

| Cell     | DRC | LVS | GDS Export | Notes |
|----------|-----|-----|------------|-------|
| Inverter | ✅  | ✅  | ✅         | Clean and minimal |
| NOR      | ✅  | ✅  | ✅         | Ready for datapath use |

I do plan on pasting the entirety of the library here once I have completely done the processor.

🎯 Current Focus

This phase of the project focuses on:
 Building custom layout blocks for a 64-bit RISC-V datapath
 Understanding and resolving DRC, LVS, and RCX errors
 Mastering Cadence Virtuoso workflows
 GDS export and documentation

Testbenches and simulation infrastructure will be added in later stages.


   🔍 Viewing the GDS Files

You can view these layout files using [KLayout](https://www.klayout.de/):

Yashas Yadav S
USN: 1JT22EC120
Electronics and Communication Engineering
VTU – Jyothy Institute of Technology, Bengaluru
