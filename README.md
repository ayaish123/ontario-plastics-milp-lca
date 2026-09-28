# MILP–LCA model for plastics recycling infrastructure planning in Ontario

This repository contains the optimization code and input data used to reproduce the base case and the S0–S5 scenario and sensitivity analyses from:

**Yaish, A.M.Y., Zhang, Q., Yang, L., McLellan, P.J.**  
*Optimizing facility siting, technology selection, and feedstock allocation for plastics recycling using life cycle assessment integrated with mixed-integer linear programming.*

The model integrates life cycle assessment (LCA) with mixed-integer linear programming (MILP) to evaluate regional plastics recycling infrastructure in Ontario, Canada. It considers technology selection, facility siting, regional feedstock allocation, transportation, product fulfillment, virgin/reference-product provision, and residual landfill fate.

## Repository contents

- `MILP_LCA__S0_S5.ipynb`  
  Jupyter notebook that loads the published optimization data, solves the base case, and reproduces the S0–S5 scenario and sensitivity analyses.

- `Optimization formulation.xlsx`  
  Supplementary workbook containing the optimization matrices, vectors, bounds, impact coefficients, and supporting data required by the notebook.

The notebook and Excel workbook should be placed in the **same directory**.

## Analyses reproduced

The notebook reproduces:

- **S0** – Base case
- **S1** – Portfolio transition constraint
- **S2A** – Dissolution emphasis
- **S2B** – Advanced PET pathway emphasis
- **S2C** – Mixed-plastic-waste catalytic fast pyrolysis emphasis
- **S2D** – Incineration placement
- **S3** – Combined siting flexibility
- **S4** – H-matrix hotspot sensitivity
- **S5** – Supply availability scaling

The notebook reports the optimized environmental objective, selected facility portfolio, available and processed feedstock, residual landfill, and related scenario metrics.

For S5, the output also includes the environmental objective normalized per tonne of available feedstock and per tonne processed.

## Requirements

The notebook requires:

- Python 3
- NumPy
- pandas
- openpyxl
- Jupyter Notebook or JupyterLab
- Gurobi Optimizer
- `gurobipy`
- a valid Gurobi license

Example package installation:

```bash
pip install numpy pandas openpyxl jupyter gurobipy
