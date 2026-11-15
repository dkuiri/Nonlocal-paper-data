# Nonlocal Transport Signatures of Topological Superconductivity in a Phase-Biased Planar Josephson Junction

This repository contains the numerical data and Jupyter notebooks used in our theoretical study of nonlocal transport in planar Josephson junctions.

The work investigates how nonlocal conductance can be used to identify topological phase transitions in superconducting hybrid systems. In particular, we show that the topological transition is accompanied by a change in the sign of the nonlocal conductance at zero energy.

We also investigate how the Zeeman interaction affects the relationship between applied magnetic flux and the superconducting phase difference, and how this influences the accessibility of the topological regime.

**Publication:** Physical Review B 108, 205405 (2023)

**Authors:** D. Kuiri and M. P. Nowak

---

## 1. Introduction

Planar superconductor-normal-superconductor (SNS) Josephson junctions are promising platforms for studying topological superconductivity and Majorana bound states.

In this work, we theoretically investigate nonlocal transport as a probe of topological phase transitions in phase-biased planar Josephson junctions.

Our main findings are:

- The nonlocal conductance is closely related to the quasiparticle band structure of the junction.
- The closing and reopening of the superconducting gap at zero momentum are accompanied by a change in the sign of the nonlocal conductance at zero energy.
- This sign change originates from the change in the electron-like and hole-like character of the quasiparticle bands.
- The Zeeman interaction strongly influences the magnetic flux-to-phase conversion.
- Phase slips can prevent the junction from reaching the phase difference required for the topological regime, particularly at weak in-plane magnetic fields.

## 2. Physical Model

We consider a two-dimensional semiconductor strip coupled to two superconducting electrodes, forming a planar SNS Josephson junction.

The model includes Rashba spin-orbit coupling, Zeeman interaction and proximity-induced superconductivity. The superconducting electrodes have a phase difference phi, which can be controlled using magnetic flux.

The system is described by the Bogoliubov-de Gennes Hamiltonian:

\[
\begin{aligned}
H={}&
\left(
\frac{\hbar^2 k_x^2}{2m^*}
+\frac{\hbar^2 k_y^2}{2m^*}
-\mu
\right)\sigma_0\otimes\tau_z\\
&+g(x)\mu_B B\sigma_y\otimes\tau_0\\
&+\alpha(x)(\sigma_x k_y-\sigma_y k_x)\otimes\tau_z\\
&+\Delta(x)\tau_+
+\Delta^*(x)\tau_- .
\end{aligned}
\]

Here, sigma and tau matrices act on the spin and electron-hole degrees of freedom, respectively.

The superconducting pairing potential is spatially dependent:

\[
\Delta(x)=
\begin{cases}
\Delta_0, & x<-L_j/2,\\
0, & |x|\leq L_j/2,\\
\Delta_0 e^{i\phi}, & x>L_j/2.
\end{cases}
\]

The material parameters are chosen to describe an InSb semiconductor proximitized by aluminium.

| Parameter | Value |
|---|---:|
| Effective mass | 0.014 me |
| Chemical potential | 5 meV |
| Superconducting gap | 0.2 meV |
| Rashba coupling | 50 meV nm |
| Junction length | 80 nm |
| Junction width | 2000 nm |
| Lattice spacing | 10 nm |

## 3. Numerical Approach

The Hamiltonian is discretized on a square lattice, and the numerical calculations are performed using the Kwant quantum transport package.

Three configurations of the junction are considered.

### 3.1 Open SNS Junction

The open junction is connected to top and bottom normal-metal leads.

We calculate the scattering matrix and electron and hole transmission probabilities to investigate nonlocal transport.

The nonlocal conductance is given by

\[
G_{ij}(E)=\frac{e^2}{h}
\left[
T_{ij}^{ee}-T_{ij}^{he}
-\delta_{ij}N_i^e
\right].
\]

For transport between different leads, this becomes

\[
G_{12}(E)=\frac{e^2}{h}
\left(T_{12}^{ee}-T_{12}^{he}\right).
\]

Here, the two transmission contributions describe electron transmission and crossed Andreev reflection.

### 3.2 Isolated SNS Junction

We also consider a finite isolated junction by disconnecting the normal leads.

This configuration is used to calculate:

- Andreev bound-state energies
- Spin polarization of the bound states
- Magnetic-field-dependent energy spectra
- Supercurrent and current-phase relations

### 3.3 Translation-Invariant Junction

To investigate the band structure, we consider a junction that is translation invariant along the transverse direction.

The transverse momentum ky is then a good quantum number.

This allows us to study the electron-like and hole-like character of the quasiparticle bands and understand their connection to nonlocal transport.

## 4. Results and Discussion

### 4.1 Andreev Bound States and Nonlocal Conductance

We first investigate the Andreev bound-state spectrum of an isolated SNS junction in the presence of an in-plane magnetic field.

The Zeeman interaction splits the Andreev bound-state spectrum and modifies the phase regions associated with the topological transition.

We then calculate the nonlocal conductance as a function of energy and superconducting phase difference.

Our results show that the closing and reopening of the gap at zero energy are accompanied by a change in the sign of the nonlocal conductance.

This provides a transport signature of the topological transition.

### 4.2 Quasiparticle Charge Polarization

To understand the origin of the conductance sign change, we investigate the quasiparticle band structure.

We find that positive-energy bands are predominantly electron-like, whereas negative-energy bands are predominantly hole-like in the relevant regions of the spectrum.

The dominant transport process therefore changes between electron transmission and crossed Andreev reflection.

This explains the relationship between quasiparticle polarization and the sign of the nonlocal conductance.

We also show that not every gap closing corresponds to a topological transition. Some band crossings occur at finite momentum and do not produce the required change in the nonlocal conductance sign.

### 4.3 Magnetic Flux and Phase Biasing

In realistic Josephson junctions, the superconducting phase difference is controlled by applying perpendicular magnetic flux through a superconducting loop.

The relationship between magnetic flux and phase difference is nonlinear because of the loop inductance and the supercurrent flowing through the junction.

We investigate how the Zeeman interaction modifies the current-phase relation and consequently changes the flux-to-phase conversion.

### 4.4 Phase Slips and Experimental Limitations

An important finding of this work is that phase slips can prevent the junction from reaching the phase difference close to pi.

This creates a limitation for accessing the topological regime at relatively weak in-plane magnetic fields.

Our calculations show that stronger Zeeman interaction can modify the flux-to-phase conversion and make the required phase difference accessible.

We also investigate the dependence of this effect on the superconducting loop inductance.

These results highlight the importance of considering realistic phase-biasing conditions when designing experiments to detect topological superconductivity.

## 5. Figures and Numerical Results

The numerical calculations correspond to the figures presented in the published paper.

| Figure | Description |
|---|---|
| Figure 1 | Schematic of the planar SNS Josephson junction |
| Figure 2 | Andreev bound-state spectrum and nonlocal conductance |
| Figure 3 | Band dispersion and electron and hole probability currents |
| Figure 4 | Quasiparticle charge polarization and electron transmission |
| Figure 5 | Magnetic flux-to-phase conversion |
| Figure 6 | Numerical phase conversion and nonlocal spectroscopy |

The corresponding numerical datasets and plotting routines are included in this repository.

## 6. Repository Contents

The repository contains two main Jupyter notebooks.

**Closed junction calculations**

`S_N_S_2D_topo_closed_junction_paper_data.ipynb`

This notebook contains calculations related to the isolated junction, including Andreev bound-state spectra, eigenstates and superconducting current.

**Open junction calculations**

`S_N_S_2D_topo_open_junction_paper_data.ipynb`

This notebook contains calculations of nonlocal transport, electron and hole transmission, conductance spectra and magnetic-field-dependent results.

The repository also contains numerical datasets saved in Pickle (`.pkl`) format. These datasets are used for analysing and plotting the results without repeating all computationally expensive simulations.

## 7. Requirements

The calculations use Python and the following scientific packages:

- Kwant
- NumPy
- SciPy
- Matplotlib
- Tinyarray
- Jupyter Notebook
- IPyParallel
- Adaptive

Some calculations use parallel execution and sparse matrix solvers.

## 8. Running the Notebooks

Clone the repository:

```bash
git clone https://github.com/dkuiri/Nonlocal-paper-data.git
cd Nonlocal-paper-data
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open either of the following notebooks:

- `S_N_S_2D_topo_closed_junction_paper_data.ipynb`
- `S_N_S_2D_topo_open_junction_paper_data.ipynb`

The saved numerical datasets can also be loaded for post-processing and figure generation without repeating the full simulations.

For the complete calculations, the required Python packages and parallel computing environment must be configured.

## 9. Publication and Citation

If you use this code or numerical data in your research, please cite our paper and code:

D. Kuiri and M. P. Nowak, "Nonlocal transport signatures of topological superconductivity in a phase-biased planar Josephson junction", Physical Review B 108, 205405 (2023).

DOI: https://doi.org/10.1103/PhysRevB.108.205405

The numerical code associated with this work is also archived on Zenodo:

https://doi.org/10.5281/zenodo.8086328

---

**Dibyendu Kuiri**

Theoretical Condensed Matter Physics

[GitHub](https://github.com/dkuiri) | [Academic Website](https://dkuiri.github.io/) | [Google Scholar](https://scholar.google.com/citations?user=K1jTqmYAAAAJ)
