# cb2330-PRO1_Pair-21

For our project we used the paper “Visualization and analysis of gene expression in tissue sections by spatial transcriptomics. Science 353(6294):78-82.”, by Ståhl, P. L. et al. (2016).
The paper describes the development of the spatial transcriptomics (ST) technology. The authors measure the sensitivity of ST to capture mRNA by comparing it to smFISH. While not providing the exact formula they used, we speculate that they calculated sensitivity by averaging the mean number of transcripts captured by ST divided by the mean number of transcripts captured by smFISH (assumed to have near 100% sensitivity).  

We questioned if the sensitivity reported would be universally applicable, independent of the specific gene or the layer which it is derived from. Therefore, we pooled the means of the data given for the number of transcripts captured by ST and smFISH. In our parametric model, we first assume that the process of mRNA capture by ST follows a Poisson distribution, with the mean poisson equal to the sensitivity reported. Thereafter, we perform a Monte Carlo Simulation to obtain a mean transcript  count. We then ran the simulation backwards on the pooled data to obtain a new mean for the proposed Poisson distribution. We explored the uncertainty of our model using a likelihood interval and a bootstrap method.

In our parametric model the mean of the Poisson was lower than the sensitivity reported by the paper, potentially suggesting that the sensitivity reported is not universal and that it may vary depending on the gene and the location.

The mean count data obtained from the bar plots is imported as a table, defined as “conditions”. The initial sensitivity was set to 0.069 (reflecting the 6.9% provided in the paper). The notebook can be run in Google Colab. 
