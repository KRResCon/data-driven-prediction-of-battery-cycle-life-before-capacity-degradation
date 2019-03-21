# data-driven-prediction-of-battery-cycle-life-before-capacity-degradation

The code in this repository shows how to load the data associated with the paper 'Data driven prediciton of battery cycle life before capacity degradation' by K.A. Severson, P.M. Attia, et al. The data is available at [https://data.matr.io/1/](https://data.matr.io/1/).

This analysis was originally performed in MATLAB, but here we also provide access information in python. In the MATLAB files (.mat), this data is stored in a struct. In the python files (.pkl), this data is stored in nested dictionaries.

The data associated with each battery (cell) can be grouped into one of three categories: descriptors, summary, and cycle.
- **Descriptors** for each battery include: charging policy, cycle life, barcode and channel. Note that barcode and channel are currently not available in the pkl files).
- **Summary data** include information on a per cycle basis, including cycle number, discharge capacity, charge capacity, internal resistance, maximum temperature, average temperature, minimum temperature, and chargetime.
- **Cycle data** include information within a cycle, including time, charge capacity, current, voltage, temperature, discharge capacity. We also include derived vectors of discharge dQ/dV, linearly interpolated discharge capacity and linearly interpolated temperature.

The `LoadData` files show how the data can be loaded and which cells were used for analysis in the paper. 
