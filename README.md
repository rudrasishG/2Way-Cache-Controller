**2-Way Cache Controller**

**Overview**

This project implements a 2-way set associative cache controller using SystemVerilog. The controller handles read/write operations, manages cache hits and misses, and interacts with main memory. The design flow includes RTL coding, simulation, synthesis, and physical layout using OpenLane and KLayout.

The uploaded KLayout image shows the physical layout of the cache controller after a successful OpenLane run.

**PROJECT STRUCTURE**

Verilog Modules:

cache_controller.v – Top-level cache controller module that integrates all submodules.

tag_array.v – Maintains tags for cache lines to check hits/misses.

data_array.v - Maintains data lines from and to cpu/memory.

fsm_logic.v – Finite State Machine managing cache operations and memory interface.

lru_array.v – Implements Least Recently Used replacement policy for the 2-way cache.

**RUN FOLDER:**

Contains OpenLane outputs, including synthesis reports, placement and routing, and GDSII files.

cache_controller.klayout.gds – The final GDS layout.

**DESIGN FLOW**

**RTL Design**

Written in Verilog using modular design principles.

Simulated using ModelSim to verify functionality for read/write operations, hit/miss logic, and LRU updates.

**Synthesis**

Synthesized using Yosys in the OpenLane flow.

Generated gate-level netlist for physical design.

**Floorplanning & Placement**

OpenLane automatically placed cells to optimize timing and area.

Constraints applied for clock, I/O, and core utilization.

**Routing & DRC/LVS**

Routed using OpenLane's automated tools.

Generated final GDSII file, verified for design rule compliance.

**KLayout Visualization**

Loaded the .gds file in KLayout to visualize physical layout.

The layout shows all standard cells, interconnects, and I/O pins clearly.
