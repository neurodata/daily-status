# Daily Report 20170417
Jesse Leigh Patsolic  



## MEDA Timing and Profiling
Today I ran system.time on meda with a sample of size 1000.  For this
first run I forgot to restrict mclust to "VVV", so it ran all 
11 models.  (I did try it wtih just "VVV", it gave 2 
clusters and wasn't worth timing)


### Sample size 1e3

[meda times samp 1e3](./meda_timetest_samp1e3.txt)  
[Hierarchical Clustering samp 1e3 w/11 models](./hmcTreeVVV1e3_Rprof.txt)  


### Sample size 1e4
[meda times samp 1e4](./meda_timetest_samp1e4.txt)  
[Hierarchical Clusterin samp 1e4](./hmcTreeVVV1e4_Rprof.txt)  
[outliers samp 1e4](./outliers_Rprof_1e4.txt)  
[Heatmaply samp 1e4](./heatmaply_Rprof_1e4.txt) 


## [EM Algorithm](./em1.html)

I also ran MC [simulations](./em1.html)
for parameter estimates for a misture of two
Gaussians.  My implementation seems to do fine when the means are far
apart i.e. -4 and 3.  If they get close than that, my implementation
crashes (the class conditional responsibilities are either all 0 or 1,
the mean estimates invole NANs, or the class conditional SDs = 0).

I'll read F&R some tonight and see if that helps. 




