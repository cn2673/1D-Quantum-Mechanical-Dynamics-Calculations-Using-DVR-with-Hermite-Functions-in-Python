# 1D Quantum Mechanical Dynamics Calculations Using DVR with Hermite Functions in Python

**"Arginine: II. Interactions of Its Salt Bridges with Branched Aliphatic Side Chains"**

The code is based on the DVR formulation of the solutions by Bačić and Light [Annu. Rev. Phys. Chem. 40 (1989) 469-498].

This repository contains Python code for performing 1D quantum dynamics calculation of vibrational states in a predefined potential. In our example, we used it for a double-well potential, a fitted quartic potential obtained from ab initio points. The method uses a **finite basis representation (FBR)** of Hermite functions, which is transformed into a **discrete variable representation (DVR)** via diagonalization of the position operator.

This method enables the construction of the full quantum Hamiltonian—including both kinetic and potential energy terms. The DVR transformation allows for a straightforward computation of the potential energy and efficient diagonalization of the total Hamiltonian. 

This approach is commonly used to study proton tunneling, hydrogen transfer, and vibrational dynamics in low-dimensional quantum systems, such as those found in salt bridges, biomolecular hydrogen bonds, and model tunneling coordinates.

## The main notebook is located in: 

notebooks/1D-quantum-mechanical-calculations.ipynb

## What’s Implemented:
- Construction of matrices in **finite basis representation(FBR)**
- Diagonalization of the position operator to obtain DVR grid points
- Transformation of the kinetic energy operator from FBR to DVR
- Evaluation of defined potential
- Assembly of the full Hamiltonian matrix in DVR
- Computation of vibrational eigenvalues and wavefunctions
- Projection of wavefunctions onto a real-space grid
- Normalization and visualization of the quantum states

## Precomputed 50 quad point matrices
data_files/Q_matrix.txt  - Position operator matrix (FBR)

data_files/K_raw_matrix.txt - Raw kinetic energy matrix (Hermite basis)

data_files/KE_matrix.txt  - Final kinetic energy matrix (DVR + mass-scaled)

## Computational Note
Running the notebook with n = 50 quadrature points (basis functions) is computationally intensive and may take 10–15 minutes depending on your machine or Google Colab session.

## Requirements

- Python 3.8+
- NumPy
- SciPy
- Matplotlib
- mpmath

Install everything with:

```bash
pip install -r requirements.txt
