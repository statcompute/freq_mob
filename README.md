#### Introduction

To mimic the py\_mob package (https://pypi.org/project/py-mob) for binary outcomes, the freq\_mob is a collection of python functions that would generate the monotonic binning and perform the variable transformation for frequency outcomes such that the Pearson correlation between the transformed $X$ and $Ln(Y)$ is equal to 1. In case of frequency count models with the $Log()$ link function, the transformation function is derived as $F(x)_i = Ln \frac{\sum_i Y / \sum_i Exposure}{\sum Y / \sum Exposure}$ in the training sample, where $Exposure$ is the number of cases and $i$ refers to the $ith$ bin groupped by $x$ values.  


Should you have any question or suggestion about the freq\_mob package, please feel free to drop me a line.

#### Core Functions

```
freq_mob
  |-- qtl_bin()  : An iterative discretization based on quantiles of X.  
  |-- cnt_bin()  : A revised iterative discretization for records with Y > 0.
  |-- iso_bin()  : A discretization algorthm driven by the isotonic regression between X and Y. 
  |-- rng_bin()  : A revised iterative discretization based on the range of X values.  
  |-- kmn_bin()  : A discretization algorthm based on the kmeans clustering of X.  
  |-- gbm_bin()  : A discretization algorthm based on the gradient boosting machine.  
  |-- view_bin() : Displays the binning outcome in a tabular form. 
  |-- cal_newx() : Applies the variable transformation to a numeric vector based on the binning outcome.
  `-- mi_score() : Calculates the mutual information score between X and Y.
```

###  Authors

[WenSui Liu](mailto:liuwensui@gmail.com) is a seasoned data scientist with 15-year experience in the financial service industry. 

[Joyce Liu](mailto:jcl4482@my.utexas.edu) is a college student majoring in Mathematics. 
