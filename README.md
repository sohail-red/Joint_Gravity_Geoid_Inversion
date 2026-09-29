# Joint Gravity–Geoid Inversion

A Python-based framework for **joint inversion of gravity and geoid observations** to estimate subsurface density distribution.

---

## Overview
The workflow includes:

1. Data preparation and preprocessing
2. Gravity forward modelling
3. Geoid forward modelling
4. Construction of gravity and geoid objective functions
5. Joint gravity–geoid inversion
6. Synthetic-data experiments
7. Visualization and analysis of inversion results

---

## Repository Structure

```text
.
├── input/
│       Contains all input data required for filtering, preprocessing, and inversion.
│
├── data_preparation.ipynb
│       Defines the model domain, selects the prior model, and prepares the data vectors.
│
├── joint_inv_main.ipynb
│       Main notebook for performing the joint gravity–geoid inversion.
│
├── joint_inv_synthetic.ipynb
│       Performs synthetic-data experiments and validates the joint inversion framework.
│
├── sh_geoid.ipynb
│       Performs spherical harmonic analysis of global geoid data.
│       Filtered results are saved in the input/pysh/ directory.
│
├── sh_gravity.ipynb
│       Performs spherical harmonic analysis of global gravity data.
│       Filtered results are saved in the input/pysh/ directory.
│
├── kernels.py
│       Computes the forward-model kernels used in the inversion.
│
├── objective_function.py
│       Defines the augmented objective function to be minimized during the inversion.
│
├── lsqr.py
│       Contains the main inversion solver.
│
└── tesseroid_grav_inversion_lib.py & InvPlot_library
        Provides supporting functions for tesseroid based gravity inversion and Visualisation.

