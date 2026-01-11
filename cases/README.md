# Benchmark Cases

The Benchmark cases are based on the B size grid model.

## Steady-State Cases

Before running transient cases, it is recommended to run the steady-state cases `steady` and `TFM-steady`. These two cases calculate the steady-state air flow field based on SIMPLE and can be mapped to the initial conditions of transient cases to accelerate the convergence of transient cases. Specifically:

- `steady` is the steady-state case for `STM-1`/`STM-2`/`STM-3`/`MM`
- `TFM-steady` is the steady-state case for `TFM`


## Transient Cases

The names of the transient cases are consistent with the five methods in the paper, which are:

- `STM-1`: Based on scalar transport model and empirical saltation layer
- `STM-2`: Based on scalar transport model and turbulent dissipation source term
- `STM-3`: Based on scalar transport model and canopy source term
- `MM`: Based on mixture model
- `TFM`: Based on two-fluid model


## Running Cases

Enter the case directory, for example `STM-1`:
```bash
cd STM-1
```

Run serial case (recommended):
```bash
./Allrun
```

Run parallel case:
```bash
./Allrun-parallel
```

## Reference Data

The `rawData` folder contains measured or experimental data for comparison.