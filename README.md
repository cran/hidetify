## Hidetify - High dimensional Influence Measure

### What is Hidetify?
Hidetify is a high dimensional influence measure for identifying influential observations in high dimensional linear regression (number of features equal or greater than the number of samples). This package comes with the paper (Multiple detection of influential observations in high dimensional linear regression) describing the details of the procedure.

The package provides two main features.

# Single Outlier Detection 
The module <code> shidetify </code> apply a single outlier detection method to the data. Caution is required in the application of this method. Indeed, there is often a risk that the data may be affected by the adverse effects of swamping and masking. Unless you are sure of what you are doing, it is suggested that you use the <code> mhidetify </code> module. 

# Multiple Outlier Detection 
The module <code> mhidetify </code>  applies a group deletion procedure to mitigate the dual phenomenon of masking and swamping effects. It consists of three steps. The first stage applies an ultra conservative score to mitigate the swamping effect, the second stage uses the clean sample generated in the previous stage and applies an aggressive score to attenuate the masking phenomenon. Finally, the last step is concerned with the validation of the influential set generated by the two previous steps. The procedure is repeated iteratively until convergence is achieved. 