# POMDPModels

This package provides the following models for POMDPs.jl:

* Grid World
* Tiger
* Crying Baby
* Random 

## Installation
Make sure POMDPs.jl is installed, then run the following code in the Julia REPL:
```julia
using POMDPs
Pkg.add("POMDPModels")
```

## Usage

To use POMDPModels, simply load it and initialize a model. The model supports the basic functions required by many of
the JuliaPOMDP solvers. For example:

```julia
using POMDPModels

pomdp = TigerPOMDP()
# do what you would do with a POMDP model, for example use QMDP to solve it
using QMDP
solver = QMDPSolver()
policy = solve(solver, pomdp) # compute a pomdp policy
```

You can initialize the other pomdp types in the module in the following way:
```julia
using POMDPModels

pomdp = TigerPOMDP()
pomdp = BabyPOMDP()
pomdp = RandomPOMDP()

mdp = GridWorld()
mdp = RandomMDP()
```
