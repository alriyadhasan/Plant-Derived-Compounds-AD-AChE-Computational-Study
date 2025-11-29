# Plant-Derived-Compounds-AD-AChE-Computational-Study
This repository contains data and workflows for identifying plant-derived acetylcholinesterase inhibitors for Alzheimer's disease. Using molecular docking, MM-GBSA, DFT analysis, and molecular dynamics simulations, we evaluate and identify promising compounds that may serve as novel, natural treatments for Alzheimer's disease.
# AD-AChE-Ligand-Docking-Simulation

## Overview

This repository contains data and workflows for identifying plant-derived acetylcholinesterase inhibitors for Alzheimer's disease. Using molecular docking, MM-GBSA, DFT analysis, and molecular dynamics simulations, we evaluate and identify promising compounds that may serve as novel, natural treatments for Alzheimer's disease.

## Authors
- Al Riyad Hasan, Sohel Rana, Alok Kumer, Nazmul Hossain, Sabekun Nahar Sezin, Md. Tarikul Islam, Nazim Uddin Molla, Md. Nazir Hosen, Nusrat Mahjabin Maha, Marzia Mahzabin Mahi, Symon Saroar, Md. Aktaruzzaman**, Md. Obayed Raihan*

**Correspondence:**  
- Md. Aktaruzzaman (Email: aktaruzzaman.phar@gmail.com)  
- Md. Obayed Raihan (Email: mraihan@csu.edu)  

## Repository Structure

/data
ligands/ # 440 screened phytochemicals
top_compounds/ # Top 3 compounds + control donepezil
supplementary/ # Tables, PDFs, Excel files

/docking
SP_docking/ # Standard Precision docking results
XP_docking/ # Extra Precision docking results
MMGBSA/ # Post-docking binding free energies

/qm_analysis/ # DFT and Frontier Molecular Orbital analysis
/md_simulations/
trajectories/ # MD trajectories
analysis/ # RMSD, RMSF, Rg, SASA, PCA, FEL, DCCM plots

/code/ # Scripts for analysis and plotting
/figures/ # Figures from manuscript
README.md
LICENSE
.gitignore

## Methodology Summary

1. **Ligand Library Preparation:** 1,577 phytochemicals curated from 35 medicinal plants; 440 selected based on ADMET properties.
2. **Protein Preparation:** Human AChE (PDB ID: 7E3H) prepared using Schrödinger Maestro with OPLS4 force field.
3. **Docking:** SP and XP docking using Glide; top compounds rescored with Prime MM-GBSA.
4. **QM Analysis:** DFT calculations using Gaussian09; HOMO/LUMO, ΔEgap, and other frontier orbital properties computed.
5. **ADMET & Toxicity:** SwissADME and ProTox-III used to assess drug-likeness and toxicity.
6. **MD Simulations:** 100 ns simulations with Desmond; analyzed RMSD, RMSF, Rg, SASA, PCA, FEL, DCCM.

## How to Reproduce

1. Clone the repository:
```bash
git clone https://github.com/YourUsername/AD-AChE-Ligand-Docking-Simulation.git
cd AD-AChE-Ligand-Docking-Simulation
Use the files as follows:

data/ligands → input for docking

docking/SP_docking and docking/XP_docking → docking outputs

qm_analysis → DFT calculations

md_simulations/trajectories → input for trajectory analysis

md_simulations/analysis → MD plots and metrics

Optional: use code/ scripts to generate additional analysis plots.

License

Code: MIT License

Data: CC BY 4.0 (free to use with attribution)
Citation

Hasan AR, Rana S, Kumer A, et al. Uncovering Plant-Derived Compounds to Treat Alzheimer's Disease by Targeting the Acetylcholinesterase Enzyme through Computational Studies. GitHub Repository: https://github.com/YourUsername/AD-AChE-Ligand-Docking-Simulation
