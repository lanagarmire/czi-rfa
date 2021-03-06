# Aim 3:

**To evaluate the extent to which latent space arithmetic works in HCA benchmark datasets generated under this or other initiatives.**

## Background

Latent features describe a lower dimensional representation of input data and there are many methods, including principal components analysis (PCA) and non-negative matrix factorization (NMF), that arrive at unique solutions.
Certain classes of deep generative models, including variational autoencoders (VAEs) and generative adversarial networks (GANs), that add a distribution matching constraint, imbue intuitive mathematical features to the learned latent features [1,2].
For instance, a GAN learned latent features that could be manipulated with arithmetic: Subtracting out the essence of a smile from a woman and adding it to a neutral man resulted in an image vector of a smiling man [3].
We will assess the extent to which single cell gene expression latent spaces aggregated from deep generative neural networks can be manipulated mathematically.
We will explore how these properties enable rapid biological discovery regarding cell-type, cellular differentiation, and the ability to generate hypothetical cells under simulated perturbation.
The _working hypothesis of this aim_ is that the latent space will preserve vector arithmetic operations between state transitions within benchmark perturbation expression datasets. 

## Approach

We will use the latent space derived from our deep unsupervised neural networks to interrogate cell-type transitions under exogenous perturbation.
We describe two experiments using data generated by Arjun Raj's group, but we can test our latent space methods using other HCA benchmark datasets with similar properties.

First, as a hypothetical example to test our approach, we will obtain the latent space projections of isolated human fibroblasts and cardiomyocytes.
The differentiation of cardiomyocytes from fibroblasts is well studied, and the driving transcription factors have been identified [4].
We will subtract the mean latent space representation vector of fibroblasts from the cardiomyocyte latent vector.
We hypothesize that the largest features diffentiating the two latent space vectors will be involved with the key transcription factor networks (Gata4, Mef2c, and Tbx5) known to drive the transition.

Additionally, we will test large gene expression screens of homogenized cell-types assayed under various molecular perturbations.
Much like with the "essense of a smile", we will determine if we can identify "the essense of a perturbation".
We will subtract the encoded latent vectors of a series of normal cell-types from the corresponding cell-type under perturbation.
The resulting latent space vector should provide the essense of the specific perturbation.
We will then test if adding the resulting latent vector back to a held out normal cell-type results in a representation near the perturbed cell-type.
As a negative control, we will perform all subtractions in raw gene expression space.
We will also compare our approach to other latent space representations including PCA, NMF, and other methods derived from the CZI collective.

## References:

1.	Kingma, D. P. & Welling, M. Auto-Encoding Variational Bayes. ArXiv13126114 Cs Stat (2013).
2.	Goodfellow, I. J. et al. Generative Adversarial Networks. ArXiv14062661 Cs Stat (2014).
3.	Radford, A., Metz, L. & Chintala, S. Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks. ArXiv151106434 Cs (2015).
4.  Ieda, M. et al. Direct Reprogramming of Fibroblasts into Functional Cardiomyocytes by Defined Factors. Cell 142, 375–386 (2010).
