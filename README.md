# FourRussiansRNA
Implementation of the Two Vector and Four Russians techniques for accelerating RNA folding prediction. The speedup makes the algorithm go from a **O(n^3)** to a **O(n^3/log(n))** time complexity.
The algorithm used is described in [Venkatachalam et al. paper](https://almob.biomedcentral.com/articles/10.1186/1748-7188-9-5).

The algorithm was implemented in C++. We've also implemented Nussinov's algorithm in order to test the speedup. Note that after cross-validating, we found that the best size of q is log in base 2 of n. This is thus the default size of q chosen.

## Presentation
[Here](https://github.com/YannDubs/FourRussiansRNA/blob/master/OnlyThreeRussians.pdf) You can find an intuitive explanation of the two-vectors acceleration, as well as our results.

## Code
The code can be found [here](https://github.com/YannDubs/FourRussiansRNA/tree/master/FourRussiansRNA) simply compile and run. Note that you can specify the files containing the sequences in the main().

## Results
Here are the 2 plots we generated:

![](Results/NussinovVSRussians.png)
![](Results/effectQrussians.png)
