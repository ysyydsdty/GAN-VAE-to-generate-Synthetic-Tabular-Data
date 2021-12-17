# GAN and VAE to generate Synthetic Tabular Data

## Techniques used

* Modeling Techniques: Conditional tabular GAN (CTGAN), Tabular VAE (TVAE)
* Tech Stack: Python, sdv, [Synthetic Data Vault](https://github.com/sdv-dev/CTGAN)


## CTGAN & TVAE

Modeling tabular data poses unique challenges for GANs, causing them to fall short of the baseline methods on a number of metrices such as likelihood fitness and machine learning efficacy of the synthetically generated data. The challenges include the need to simultaneously model discrete and continious columns, the multi-modal non-Gaussian values within each continuous columns and the severe imbalance of categorical columns. To address these challenges CTGAN and TVAE have been developed.

Conditional tabular GAN (CTGAN) is a GAN based method to model tabular data distribution and sample rows from the distribution. Mode-specific normalization is invented to overcome the non-Gaussian and multimodal distribution. A conditional generator and training-by-sampling technique is designed to deal with the imbalanced discrete columns. Full-connected networks and several recent techniques are also used to train high-qulity model.

Variation autoencoder is another neural network generative model. Here tabular Variational Autoencoder (TVAE) is built by adapting variational autoencoder for mixed-type tabular data generation and using the same preprocessing and modifying the loss. 
 

## Mathematical functions used for dataset generation

* Single-variable trigonometric function -> f(x)=cos(x)
* Concentric disks of 2 different classes
* Multi-variable trigonometric/exp function -> f(x,y)=sin(x)+sin(y), f(x,y)=exp(x)+exp(y)

  
 ## Performance comparison between CTGAN and TVAE

We trained CTGAN and TVAE on a few datasets of different mathematical functions as decribed in earlier section. Next we generated the syhthetic data and visually compared the generated datapoints with the training datapoints to estimate the performance. In all cases we found the performance TVAE is much better than CTGAN.

## References

* Xu, L., Skoularidou, M., Cuesta-Infante, A., & Veeramachaneni, K. (2019). Modeling tabular data using conditional gan. [arXiv preprint arXiv:1907.00503](https://arxiv.org/abs/1907.00503).












