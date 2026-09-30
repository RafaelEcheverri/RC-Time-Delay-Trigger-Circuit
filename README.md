# RC Time-Delay Trigger Circuit — LTSpice, PCB (Team Project)

A resistor-capacitor (RC) time-delay circuit designed to trigger a PCB's status LED after a fixed delay following a switch press, simulated in LTSpice and validated through physical lab testing.

> **Note:** This repository contains documentation only. The original LTSpice `.asc` simulation file and PCB design files were not preserved from the original lab submission, so no source/schematic files are included here — only a written description of the design and results.

## Project overview

This was a two-person lab project (collaborated with a partner) for a Linear Circuits course, focused on designing and validating a first-order RC timing circuit.

### Goal

Design an RC circuit that, after a switch is pressed, waits a fixed delay before triggering a PCB's LED — specifically, achieving a **15-second delay** once the capacitor's voltage reaches a **3.5V reference voltage**, charging from a 10V source.

### Design approach

1. **Derivation** — Starting from the standard RC charging equation:

   V(t) = V_source × (1 − e^(−t / RC))

   solved for the RC time constant needed to reach the 3.5V reference at t = 15 seconds, given a 10V source.

2. **Component selection** — Based on the derived RC time constant, selected a **100 µF capacitor** and a **348 kΩ resistor** to achieve the target delay.

3. **Simulation** — Modeled the circuit in LTSpice to confirm the derived component values produced the expected 15-second delay before reaching 3.5V.

4. **Physical testing** — Built and tested the circuit on a lab PCB, TA-supervised, measuring the actual time to trigger across repeated trials.

### Results

- Simulated delay matched the derived target of 15 seconds.
- Physical trials consistently triggered around **~13 seconds**, landing within roughly **0.8×–1.2×** of the target across repeated tests.
- The discrepancy between simulated and real-world timing was attributed to non-ideal component behavior (tolerance variation in the real resistor/capacitor values compared to their ideal simulated values).

## Tools

- **Simulation:** LTSpice
- **Hardware:** Discrete RC components on a lab PCB

## Background

Completed as Project 2 ("Time Delayed Circuits") in a Linear Circuits I lab course, in collaboration with a lab partner.
