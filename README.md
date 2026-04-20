# BAR_ManyToOne
This document serves as a brief guide for the use of the R analysis program included in the study "Bayesian Adaptive Randomization Design for many-to-one comparison in multi-arm clinical trials".

# The brief guide to use the R code
The document folder BAR_ManyToOne contains 4 R functions "wei_F30_runtrial.r, wei_modelsparameter.r, function.r, wei_F30_trial.r" and a result document.
In the wei_F30_runtrial.r, you need to give a setting as follows:
1. Pu=0.928        # the parameter for selection (Please see Table 2) 
2. scenario=1;     #1-7
3. fn1="DBCD"      #AR;DBCD
4. fn2="C2"        #ER: C1=0; AR:C1=1;C2=n/2N
5. fn3="control"   #control：delta=0;control_10: delta=10
6. fn4="C3"        #DBCD:C3=2
7. file path, for example, path = file.path('D:/Rcode/BAR_ManyToOne')
 
After running the function wei_F30_trial in wei_F30_runtrial.r, the results will given in a csv file. The results contain
V1/ V2: average/ standard deviation of
na: number of pts in arm a (control group)
nb: number of pts in arm b
nc: number of pts in arm c
Na: the probability of being selected as the best arm (PS)
Nb: the probability of being selected as the best arm (PS)
Nc: the probability of being selected as the best arm (PS)
mua: average posterior PFS of arm a
mub: average posterior PFS of arm b
muc: average posterior PFS of arm c
