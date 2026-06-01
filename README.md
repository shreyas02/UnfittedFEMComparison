# Unfitted FEM Comparison Notebook

This repository contains a Julia notebook workspace for comparing unfitted finite element methods on a common embedded geometry using `Gridap.jl` and `GridapEmbedded.jl`.

The main artifact is [notebook1.ipynb](/home/shreyas-linuxmint/data/unfittedFEM/notebook1.ipynb), which is structured as a tutorial:

- shared background mesh, geometry, and model problem
- method-specific implementations on the same domain
- side-by-side comparison of unfitted discretization strategies

The current notebook compares methods on the same Poisson problem with weakly imposed Dirichlet data on an embedded boundary. The goal is to keep the continuous problem fixed and vary only the unfitted discretization.

## Contents

- [notebook1.ipynb](/home/shreyas-linuxmint/data/unfittedFEM/notebook1.ipynb): main comparison notebook
- [Project.toml](/home/shreyas-linuxmint/data/unfittedFEM/Project.toml): Julia environment for the notebook
- `EmbeddedBenchmark.jl/`: cloned reference repository used as a code and formulation base for some method implementations

## Requirements

The notebook environment currently depends on:

- `Gridap`
- `GridapEmbedded`
- `IJulia`

## Usage

Activate the environment and open the notebook with Jupyter or IJulia:

```julia
import Pkg
Pkg.activate(".")
Pkg.instantiate()
```

Then run the cells in order, since later method blocks depend on the shared setup defined earlier in the notebook.

## Notes

- Generated VTK output files are ignored in Git via `.gitignore`.