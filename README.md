# Human DPP-4 Molecular Dynamics Simulation

## Overview

This repository documents a molecular dynamics simulation of the extracellular domain of human dipeptidyl peptidase-4 (DPP-4) using GROMACS.

The protein was prepared as a solvated system and simulated in explicit SPC/E water using the OPLS-AA force field.

## System

- **Protein:** Human dipeptidyl peptidase-4 (DPP-4)
- **Protein residues:** 39–766
- **Force field:** OPLS-AA
- **Water model:** SPC/E
- **Simulation software:** GROMACS
- **Temperature:** 300 K
- **Pressure:** 1 bar

## Molecular Dynamics Workflow

1. Protein structure preparation
2. Topology generation
3. Simulation box generation
4. Solvation with explicit water
5. Ion addition
6. Energy minimization
7. NVT equilibration
8. NPT equilibration
9. Production molecular dynamics
10. Trajectory analysis

## Production Molecular Dynamics

- **Integrator:** Leap-frog
- **Time step:** 2 fs
- **Number of steps:** 5,000,000
- **Production duration:** 10 ns
- **Temperature coupling:** V-rescale
- **Reference temperature:** 300 K
- **Pressure coupling:** Parrinello–Rahman
- **Reference pressure:** 1 bar
- **Pressure coupling type:** Isotropic
- **Coordinates saved:** Every 10 ps
- **Energy data saved:** Every 10 ps

## Repository Structure

```text
human-dpp4-md-gromacs/
│
├── README.md
│
├── structure/
│   └── protein.pdb
│
├── topology/
│   └── topol.top
│
├── mdp/
│   ├── em.mdp
│   ├── ions.mdp
│   ├── nvt.mdp
│   ├── npt.mdp
│   └── md.mdp
│
├── system/
│   ├── protein_processed.gro
│   ├── protein_box.gro
│   ├── protein_solvate.gro
│   └── protein_ion.gro
│
└── analysis/
    └── graphs/
