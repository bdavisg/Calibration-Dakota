# Calibration-Dakota
Files used for Bayesian Calibration of a FEA computer model using Dakota

training.dat is training data from EPIC samples
expdata.dat is experimental results with two experimental variables (strike velocity and strike angle) and one response (residual velocity)

perfcal.in is a Bayesian Calibration with all uncertain variables and no configuration variables. The model runs, but Dakota re-orders the variables. The .out file recommends using a use_variable_labels keyword, which is not featured in the bayesian calibration w/ surrogate method. The model does converge on reasonable values. See perf.out

perfcal2.in introduces the configuration variables and the continuous state variables for strike velocity and strike angle. The GP model does not fit and gives a response of zero for each iteration. See perf2.out.
