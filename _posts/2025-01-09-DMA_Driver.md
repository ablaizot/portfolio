---
title: "AXI Chip to Chip DMA"
date: 2025-01-09
---

### Objective
The objective is a SM to CM DMA driver that allows for a transfer speed closer to physical link speed of 5 Gb/s. The timely calibration of sensors relies on configurations being pushed from the SM to CM at speeds greater than the 25 Mpbs previously acheived.

### Status
DMA loopback test succeeded. I am now attempting to connect the DMA to the C2C bridges.

### Repositories
I wrote testbench used to evaluate read/write speeds in C++ [here](https://github.com/ablaizot/speedtest/tree/CMspeed).
The DMA firmware is found in [SM ZYNQ FW](https://gitlab.com/apollo-lhc/FW/SM_ZYNQ_FW/-/tree/c2c_dma?ref_type=heads).
The BRAMs I implemented in the command module firmware are found in [Inner Tracker DTC](https://gitlab.cern.ch/cms-tracker-phase2-data-processing/BE_firmware/inner-tracker-dtc/inner-tracker-dtc/-/tree/block_ram?ref_type=heads).

### References
I followed a [Xilinx DMA driver guide](https://xilinx-wiki.atlassian.net/wiki/spaces/A/pages/1027702787/Linux+DMA+From+User+Space+2.0) to get the loopback test working.
For more information on the Apollo blades is found on the [wiki](https://apollo-lhc.gitlab.io/). 

## Pictures
<p align="center">
<img src="/portfolio/images/Apollo.jpg" width="50%">
</p>
<p align="center">
Apollo Blades in their crate at CERN Tracker Integration Facility (TIF)
</p>