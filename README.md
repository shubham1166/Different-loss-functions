# Different loss functions
This post will explain the role of loss functions and how they work, giving a few examples of the loss functions that are famous in the past few decades.

---
## What are loss functions
Loss functions are the functions/measures of evaluation how well you algorithm models your dataset. For example, if your predictions are totally off, the loss function will give a higher value and if the predictions are predictions are good, then loss functions will give a less value. Let us look at some of the loss functions:

1. **Mean Squared error**: MSE is a very basic loss function. It’s easy to understand and implement and generally works pretty well. To calculate MSE, you take the difference between your predictions and the ground truth, square it, and average it out across the whole dataset.
**![](https://lh4.googleusercontent.com/PkcuGEUB_zLzziJ549kRvDYqioYsdo5UxWEfi4cuyH0imDvMDcdhpCE7-P-QlRJ-Y-yW0QpL-ZpsOz3U5QbzYDToZ73XIedUx6wBZzq1AulBCzyZRnLqVannQgPWpkfaouWDyNgd)**

2. **Mean Absolute error**:Mean absolute error is measured as the average of sum of absolute differences between predictions and actual observations. MAE needs more complicated tools such as linear programming to compute the gradients.
**![](https://lh5.googleusercontent.com/hoN9kczR_of3wPUVzofANC6QRSUUq2dWC8ksplXobp5dAj6wUSMh5NIr2Akb6H2cQ_zVBPSaAftPAYAEszSF8xxo4H50PGAFHPNKZnmih_A8eSLf0Lq_S-kMvCg-2WurirpSPbhl)**

3. **Mean Bias error**: The error function is kind off same as that of MSE with the only difference that we don't take squared/absolute values. This is less accurate in practice, it could determine if the model has positive bias or negative bias.
**![](https://lh6.googleusercontent.com/OHPh5SBur_JyH58IncLEmHvepwfEBNjLDNxpSLImHizVvO7k5h1iklG4ak7dJaTJvwQH4dp8KiL6XTmCjOA3JegMrSpBcAfbR8HTo12aUCgDMVgNFdmh1_ZQuGO1MM8HhE1YQrDa)**

4. **Hinge Loss/Multi class SVM Loss**: It is a loss function which is used for classification. The score of the correct category should be less than the sum of scores of all incorrect categories by some safety margin(usually one). The function is not differential but it is a convex function which makes it easy to work with usual convex optimizers used in machine learning.
**![](https://lh3.googleusercontent.com/bwzQculTuCN907fd77UscirZokzdOQVSm1Gefr7yfunoU6vc3nsKxNwb61rcFSJR3JZCEtSwYn8DYfhZeP55SqF5CZXszreSmqcM0su2RARPRhAAR_mj41S4k5SdpTpclXNwt3fN)**

5. **Cross Entropy Loss**: It is the other and the most common loss function that we use for classification problem. Precisely, we are just multiplying the log of the actual predicted probability for the ground truth class. An important aspect of this is that cross entropy loss penalizes heavily the predictions that are confident but wrong.
**![](https://lh5.googleusercontent.com/GVw2w3CqSdWsWdR-92VAeD6akvtk_BuRLXD5wgKVK43VT-GzgkTllt7IQUtb-vAYkL-M9OgIWu487QeJUpth17K0Jsi7IpwVYyyknTReIetNdDwaRxRZ3GS-6EBMVvkb3-pc6Ses)**



