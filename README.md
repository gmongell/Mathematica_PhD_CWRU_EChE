# CWRU graduate engineering notebook archive

Mathematica coursework and research explorations covering reactor networks, continuum/geometry concepts, and molecular interaction potentials. The repository name identifies the archive context, not a claim about a completed degree or publication status.

## Functions and engineering applications

| Files / family | Source-supported topic | Inferred engineering application |
|---|---|---|
| `EChE462_3CSTRsInSeriesAtDifferentTemperatures.nb`, `EChE462_CombiningTheCasesOf2And3CSTRs.nb` | Serial reactor calculations and temperature-dependent cases | Exploring reactor-network conversion and selectivity [1] |
| `EChE462_MaximizingConversionToAnIntermediateProduct*`, `EChE462__DynamicsOfANonadiabaticContinuouslyStirredTankReactor.nb` | Intermediate-product and nonadiabatic reactor studies | Candidate operating-condition and transient comparisons [1] |
| `EChE475_LaPlacePressures.nb` | Surface-area/work notes naming spherical, Kelvin, and Weaire–Phelan geometries | Exploring foam interfacial geometry and energy [2] |
| `EChE475_CoordinateSystemTransforms.nb`, `EChE475_TorroidalCoordinates.nb` | Coordinate-system notes and toroidal-coordinate exploration | Formulating geometry-dependent transport problems; the transforms file includes planning notes, not a complete transform library |
| `EChE701_ForceFieldPotentialsAlkanesEthers.nb` | Bonded, angular, torsional, and nonbonded potential expressions | Understanding parameter sensitivity for organic/polymeric materials [3] |

## Example workflow calls

Requires a Mathematica front end. From a directory set to the repository root:

```wolfram
nb = NotebookOpen[FileNameJoin[{Directory[],
  "EChE462_3CSTRsInSeriesAtDifferentTemperatures.nb"}]];
```

Inspect parameter definitions and evaluate the desired reactor cells in order. For a separate molecular-interaction session:

```wolfram
NotebookOpen[FileNameJoin[{Directory[],
  "EChE701_ForceFieldPotentialsAlkanesEthers.nb"}]]
```

These are actual Wolfram front-end function calls for opening source files, not invented repository APIs. The notebooks do not expose one consistent callable library. Inputs are cell-level kinetic constants, temperatures, volumes, geometry parameters, or force-field constants; outputs are symbolic expressions, tables, and plots. Units and dependencies must be taken from each notebook before reevaluation.

## Limits and verification

Several files have repeated copies or variants, and some stored outputs contain evaluation messages (including `Clear::ssym` in the inspected three-CSTR notebook). Start from a fresh kernel and distinguish existing output from newly reproduced calculations. `-source`/`-author` filenames may contain external demonstration material: preserve contributor attribution and inspect its terms. This documentation review did not execute Mathematica. Check nonnegative concentrations, material/energy balance closure, dimensions, and special-case solutions before drawing design conclusions. Foam discussion and coordinate headings alone do not establish a complete numerical solver.

## Review scope and software citation

Documentation reviewed on 2026-10-08 against source commit [`3811740007f7`](https://github.com/gmongell/Mathematica_PhD_CWRU_EChE/tree/3811740007f7f6dd7a6dd5ccecebeefe97e5e262). “Observed” means supported by source inspection; engineering applications are reasoned possibilities unless explicitly demonstrated. Scholarly references provide methodological context and do not certify these implementations. Runtime validation is stated separately above.

For software attribution, cite Guy Francis Mongelli, *Mathematica_PhD_CWRU_EChE*, the [repository](https://github.com/gmongell/Mathematica_PhD_CWRU_EChE), the exact commit used, and your access date. Also cite the relevant method publications and any original third-party contributors. No unverified software DOI or release version is assigned by this documentation.

## Scholarly references

1. P. V. Danckwerts (1953). “Continuous flow systems: Distribution of residence times.” *Chemical Engineering Science* 2, 1–13. [DOI: 10.1016/0009-2509(53)80001-1](https://doi.org/10.1016/0009-2509(53)80001-1). Context for interpreting ideal-flow reactor models and their limitations; an RTD fitting implementation is not claimed.

2. D. Weaire and R. Phelan (1994). “A counter-example to Kelvin’s conjecture on minimal surfaces.” *Philosophical Magazine Letters* 69, 107–110. [DOI: 10.1080/09500839408241577](https://doi.org/10.1080/09500839408241577). Background for the foam geometries named in the surface-area notes; not evidence of a complete foam solver.

3. W. L. Jorgensen, D. S. Maxwell, and J. Tirado-Rives (1996). “Development and Testing of the OPLS All-Atom Force Field on Conformational Energetics and Properties of Organic Liquids.” *JACS* 118, 11225–11236. [DOI: 10.1021/ja9621760](https://doi.org/10.1021/ja9621760). Methodological context for organic-liquid force fields and torsional/nonbonded parameters.

## Ownership and existing license notices

Copyright (c) 2025 Guy Francis Mongelli

The existing project notice declares Apache License 2.0 for project code. Documentation, prose, and figures are declared CC BY 4.0; notebook code cells are Apache-2.0 and narrative/figures CC BY 4.0. Preserve all file-level and third-party notices. This README update does not change ownership or licensing terms.
