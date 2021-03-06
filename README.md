# Sequential-minimal-optimization
=========================
Author: Ehsan Zahedinejad ezahedin@ucalgary.ca
=========================

Title:
=========================
Sequential-minimal-optimization. A matlab implementation of Sequential-minimal-optimization based on the original work from
John C. Platt 2000. See publication for more detail: http://research.microsoft.com/pubs/68391/smo-book.pdf

Benchmarks:
=========================
I have tested the code on UCI Ionosphere Data Set with a traning error less than 0.3% and confidence of more than 96% on the validation data. The training size was 200 and the validation size was 151.


Function description:
============================================
The main function is SMO(X,Y,eps,tol,type,ul,Pdata,Sigma).

Input arguments for SMO function
===========================================
1. X= The feature matrix (2d array)
2. Y= Target matrix (1d array)
3. eps= Convergence criteria--show what should the difference between lagranage multiplier between two consecutive iteration has to be to exit. Example eps=0.001 (scalar)
4. tol= Distance within that the lagrange multiplier will be mapped to zero or upper limit 'C'. Best value could be:0.001 (scalar)
5. type= What Kernel function one likes to use. Currently Linear 'L' or Gaussian function are supported 'G' (char)
6. ul= upper and lower bound for lagrange multipliers. Example [0, 1]. If the upper is infinity write [0 Inf] (1d array) 
7. Pdata= Percenateg of data being used for training data. The rest will be used for validation (scalar in terms of percentage)
8. Sigma= Gaussian variance. If liner kernel write zero. 

Output arguments for SMO function
===========================================
1. [alpha,b,TS]=SMO(X,Y,eps,tol,type,ul,Pdata,Sigma).
2. alpha= array of lagrange multipliers (1d array)
3. b= threshold value (scalar)
4. TS= training size
5. Training error= SMO prints out the error when a run is complete
6. Confidence of hypothesis= SMO prints out the confidence when a run is complete

