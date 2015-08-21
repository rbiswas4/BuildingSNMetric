# Basic Idea:

We are trying to come up with metrics that are functions of `Scheduler
variables` that will improve the science cases we are interested in. In supernovae, this has been done intuitively: We know better temporal coverage helps, better filter coverage helps and so we tend to have metrics that that reward these characteristics. What is not clear is how much we lose when we move off these ideal characteristics.

# Steps

1. Take an opsim output. Pull out the output for a field using https://github.com/rbiswas4/OpSimSummary. Look at https://github.com/rbiswas4/OpSimSummary/blob/master/example/ExploringOpSimOutputs.ipynb 
2. Use sncosmo realize_lc to realize a light curve
3. Use https://github.com/rhiannonlynne/OpsimObs to add observations
4. fit the light curves using snosmo.mcmc_lc , fixing z
5. Vary the number of observations by using opsimObs, randomly change the filters and time locations
6. Build a correlation from position to size of distance errors for which we have a formula
