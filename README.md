# FOC on TI C2000 Motor Drive

## Overview
Full Field Oriented Control (FOC) implementation from scratch on a 
Texas Instruments C2000 F28379D Launchpad with BOOSTXL-DRV8323RS 
gate driver. Covers motor parameter identification, Clarke and Park 
transforms, d-axis and q-axis current loops, velocity loop, load 
test, and full performance characterization. Drive specifications 
derived from Pendubot simulation results.

## Hardware
- TI C2000 F28379D Launchpad (LAUNCHXL-F28379D)
- TI BOOSTXL-DRV8323RS gate driver evaluation board
- BLDC motor with quadrature encoder (TBD — pending Pendubot 
  simulation drive requirements)
- Bench power supply
- Oscilloscope

## Software
- Texas Instruments Code Composer Studio (CCS)
- C (embedded firmware)
- MATLAB (pre-hardware algorithm verification)
- SPRABQ8 TI application note reference

## Project Phases
- Phase 1: Pre-hardware software — Clarke/Park transforms, 
  PI controller, SVPWM — written and verified in MATLAB
- Phase 2: CCS environment setup and LED blink verification
- Phase 3: Peripheral configuration — ePWM, ADC, eQEP
- Phase 4: Motor parameter identification — R, L, back-EMF constant
- Phase 5: Current loop closure — d-axis and q-axis
- Phase 6: Current loop bandwidth characterization
- Phase 7: Velocity loop implementation
- Phase 8: Load test
- Phase 9: Full technical report

## Key Technical Content
- Clarke transform: abc → αβ frame
- Park transform: αβ → dq frame  
- Space Vector PWM duty cycle calculation
- PI controller with anti-windup
- Current sensing via DRV8323RS inline shunt amplifiers
- Encoder-based velocity estimation via eQEP peripheral

## Status
In progress — May 2026
Hardware ordered — awaiting delivery

## Weekly Log
### Week 1 — May 25 2026
- Repository created
- Hardware ordered: LAUNCHXL-F28379D + BOOSTXL-DRV8323RS
- Pre-hardware software development started
