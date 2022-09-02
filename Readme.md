########################
Our method proposes a neural network architecture, AMGNET, which combines graph neural networks with the core ideas
from the algebraic multigrid method. In essence, this network architecture consists of a series of coarsening layers
(encoding), processing layers (processing) followed by recovery layers (decoding). The first layers perform a coarsening 
of the fine-scale input to different grid scales, from which features can be extracted through graph network blocks. 
Given this extracted information, the recovery layers reconstruct the predicted flow field through an upsampling procedure.


Airfoil dataset comes from Filipe de Avila Belbute-Peres, Thomas D. Economon, and J. Zico Kolter. Combining differentiable PDE solvers and graph neural networks for fluid flow prediction.

Cylinder dataset is generated by using Ansys Fluent

train_airfoil.py    train on airfoil training dataset
tarin_cylinder.py   train on cylinder training dataset
test_airfoil.py     test  on airfoil  test dataset
test_cylinder.py    test  on cylinder  test dataset


utils.py Contains some method functions, such as writing tecplot files

environment:
torch                     1.10.0+cu113      
torch-cluster             1.5.9                  
torch-geometric           2.0.2                   
torch-scatter             2.0.9                    
torch-sparse              0.6.12                   