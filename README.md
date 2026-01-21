# CAD and Airframe Design – Cessna 172 Wing Optimisation

## Overview
This project presents a combined CAD, CFD, and FEA-based optimisation study of a Cessna 172 aircraft wing. The work focuses on aerodynamic load prediction, structural stress analysis, and mass minimisation through a fully integrated computational workflow.

The study is motivated by aerospace structural design requirements, where weight reduction, structural integrity, and manufacturability are critical for aircraft performance and efficiency.


## Objectives
- Develop a fully parametric CAD model of the Cessna 172 wing
- Compute realistic aerodynamic loads using CFD
- Apply CFD-derived loads to structural FEA
- Perform gradient-based structural optimisation
- Minimise wing mass while maintaining allowable stress limits
- Validate aerodynamic and structural results against reference data

## Geometry
- Aircraft wing: Cessna 172
- Fully parameterised wing geometry developed in CATIA V5
- Key structural components modelled:
  - Spars
  - Skin
  - Ribs
- Geometry designed to support automated optimisation loops
- Manufacturing and design feasibility considered in parameter limits

## Computational Setup
# Aerodynamic Analysis
- CFD solver: ANSYS Fluent
- Purpose: Aerodynamic load prediction
- Output:
  - Pressure distribution
  - Spanwise wing loading
- Aerodynamic loads extracted for structural application

# Structural Analysis
- FEA environment: CATIA Generative Structural Analysis
- Analysis type: Linear static structural analysis
- Boundary conditions derived from CFD loading
- Stress constraints defined using material allowable limits
- 
## Optimisation Methodology
- Hex-dominant mesh generated using snappyHexMesh
- Boundary layer refinement with near-wall resolution suitable for SST
- Mesh sensitivity study performed:
  - Fine mesh: ~8 million cells
  - Acceptable mesh quality with minimal illegal cells
- Coarse mesh (>1.6 million cells) showed degraded mesh quality due to CAD issues



## Results
Key aerodynamic results from the fine mesh case:
- Downforce coefficient shows stable convergence
- Drag coefficient converges smoothly after initial transients
- Pitching moment dominated by pressure contribution
- Viscous contributions to pitching moment are negligible

Force and moment histories demonstrate stable steady-state behaviour.



## Flow Physics
- Strong suction peaks on the lower surfaces of the elements
- Endplate and junction flows contribute significantly to drag
- Q-criterion visualisation highlights coherent vortex structures
- Ground effect accelerates flow beneath the wing, increasing downforce



## Current Limitations
- CAD surface quality limits mesh scalability
- Full-wing simulations are computationally expensive
- Some small non-manifold features remain in the geometry



## Planned Work
- CAD cleanup and removal of non-aerodynamic features
- Half-wing symmetry simulations
- Parametric study of pitch angle
- Parametric study of ride height
- Cl/Cd trends versus pitch angle and ride height
- Improved mesh independence study
- Further flow structure analysis using Q-criterion



## Tools
- OpenFOAM
- ParaView
- MATLAB/Python/C++ (post-processing)
- FreeCAD / SALOME (planned CAD repair)



## Author
Saiyed Mudassir  
Aerodynamicist

