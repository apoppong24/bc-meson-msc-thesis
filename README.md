# B_c Meson Masses — MSc thesis and original code

[![ORCID](https://img.shields.io/badge/ORCID-0009--0009--4678--0034-A6CE39?logo=orcid&logoColor=white)](https://orcid.org/0009-0009-4678-0034)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23533575.svg)](https://doi.org/10.5281/zenodo.23533575)

**Peter Agyemang Oppong**
MSc project, School of Physics and Astronomy, University of Glasgow (submitted 2022).
Supervisor: Prof. Christine Davies.

Both editions are archived on Zenodo as versions of one record:

- **As submitted (2022)** — the PDF in this repository: https://doi.org/10.5281/zenodo.23533575
- **Revised edition (October 2026)** — the submitted text with a list of corrections and a
  postscript on the 2026 B_c* observation: https://doi.org/10.5281/zenodo.23534192

Cite as: P. A. Oppong, *B_c Meson Masses*, MSc thesis, University of Glasgow (2022),
doi:10.5281/zenodo.23533575.

This repository is the archival record of the project exactly as it was
submitted: the thesis PDF and the eight Jupyter notebooks that produced its
numbers. Nothing here has been edited or re-run. The notebooks were written
and executed on Windows with Python 3 / NumPy / Matplotlib and still contain
their original outputs and plots.

For the cleaned-up, tested and extended version of this code (automatic
eigenvalue search, P/D-wave states, fine structure, refits to PDG 2024,
B_c predictions and the follow-up paper) see
**https://github.com/apoppong24/bc-quarkonium**.

## Contents

```
thesis/Bc_Meson_Masses_MSc_thesis.pdf     the dissertation (46 pages)
notebooks/
  Numerov_Algorithm_for_3D_Schrodinger_equation_Power-law_Potential.ipynb
                      1S bottomonium, charmonium and B_c in the Martin
                      (power-law) potential; normalisation, |R(0)|²,
                      hyperfine splitting
  Logarithmic_Potential.ipynb            same for the logarithmic potential
  Cornell_Potential.ipynb                same for the Cornell potential
  Radial_Excitation_state_Power_Law.ipynb         2S and 3S states, level
  Radial_Excitation_states_Log_potential.ipynb    differences, for each
  Radial_Excitation_states_Cornell_Potential.ipynb   potential
  Potentials_plot.ipynb                  overlay of the three potentials
  Numerov_Algorithm_for_3D_Schrodinger_equation_2.ipynb
                      an early, unfinished attempt at a functional
                      Numerov/bisection solver (kept for the record)
```

## What the project did

The three-dimensional radial Schrödinger equation for a heavy quark–antiquark
pair is solved with the Numerov method for three spin-independent
potentials with the parameters of Eichten & Quigg (1994): Cornell,
logarithmic (Quigg–Rosner) and power-law (Martin). Energy eigenvalues for the
1S, 2S, 3S, 1P and 2P levels of charmonium, bottomonium and B_c are obtained,
validated against the PDG spin-averaged masses and level splittings, and the
hyperfine splitting from |R(0)|² is used to predict the pseudoscalar and
vector B_c masses: B_c(1S) = 6.2767 GeV, B_c(2S) = 6.8944 GeV (experiment:
6.2745, 6.8712) and B_c*(1S) = 6.3471 GeV.

## Running the notebooks

They need only `numpy` and `matplotlib`. Several cells use `input()` to
take a trial energy from the keyboard, and the eigenvalues were found by
hand by inspecting the wavefunction plot for three nearby trial energies —
this is the procedure described in Section 3.3 of the thesis. The refactored
repository above automates it.

## Known errata (found during the refactor)

* Table 4, Cornell cc̄ 1S: printed as 0.2657 GeV; the notebook and the
  mass in Table 5 (3.9375 = 2×1.84 + 0.2575) correspond to **0.2575 GeV**.
* Eq. (42) with the model masses reduces algebraically to eq. (40); it
  only removes quark-mass dependence if experimental cc̄/bb̄ masses are used.
* Table 15 is used twice (level splittings and B_c masses).
* "Particle Datta Group" in the last reference.

## Licence

Code (notebooks): MIT. Thesis text: © Peter Agyemang Oppong, all rights
reserved; shared here for reference.
