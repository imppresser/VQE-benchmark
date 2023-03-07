# Readme

This is the classical simulation evaluation data of [VQE](https://www.nature.com/articles/ncomms5213) on [TFIM](https://en.wikipedia.org/wiki/Transverse-field_Ising_model)(Transverse-field Ising model) model. The directory is about 1D chain TFIM. Evaluation method we use is [V-score](https://arxiv.org/abs/2302.04919), and [varbench](https://github.com/varbench/varbench/tree/main/TFIsing) is the github repository.

Here we evaluate [HVA](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.92.042303), which is a physically motivated ansatz.

## Parameters

The name of the data files (listed as `*.txt`) contains most of the parameters.

Notice: Ground State Energy is abbreviated as GSE.

* `N` is the number of spins
* `BC` is the boundtry condition
* `g` is the transverse field, $\frac{g}{J}$ in [TFIM Hamiltonian](https://en.wikipedia.org/wiki/Transverse-field_Ising_model), and $\Gamma$ in [varbench](https://github.com/varbench/varbench/blob/main/TFIsing/README.md)
* `D` is the depth of ansatz
* `Eps` is the epsilon of optimizer
* `LR` is the learning rate of optimizer
* `Optimizer` is the choice of optimizers
* `times` shows how many times we run experiments, reset after every experiment

Other parameters:

Adam Optimizer:
* `β1` exponential decay rate of first-order moment estimation
    * `Paddle` default is 0.9
* `β2` exponential decay rate of second-order moment estimation
    * `Paddle` default is 0.999

## Results

The name of the data files (listed as `*.txt`) contains Energy results, and can view data files for full results. `statistics.xlsx` contains well-organized results and `*.ipynb` shows the results with plot.

* `avg` is the average result GSE of experiments (accuracy .15f)
* `min` is the minimum result GSE of experiments (accuracy .15f)
* `Avg VarE` is the average Energy Variance result of experiments
* `VarE of Min E` is the Energy Variance result of caculating the minimum result GSE
* `Avg V_Score` is the average V_Score result of experiments
* `V_Score of Min E` is the V_Score result of caculating the minimum result GSE
* `Avg ITR` is the average iterations of experiments, this can indicate efficiency of convergence

Other results:
* `ITR` is optimization iterations, the optimization process is terminated by reaching given epislon
* `VarE` is the process variable for calculating V-score, all can be visited in data file `*.txt`
* `V-score` all can be visited in data file `*.txt`