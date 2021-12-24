StanKorea homepage

# Reading list
Main Bayesian data analysis is simulated data experiment on QI(M,C,D). Prior + likelihood as mathematical model `M`, inference algorithm as computation model `C`, observed real dataset as `D`, and quantities of interest as `QI`.

# 1. `D` Data
- BDA ch.7 explains 
- [coreset](https://tamarabroderick.com/files/broderick_2018_coresets.pdf)


## 2. `M` Mathematical model
[This](https://betanalpha.github.io/assets/case_studies/probability_densities.html#2_elementary_building_blocks) equips mathematical building blocks. Also, the reparameterization issues are addressed with great importance which affects the subsequent computation. Starting from five elementray blocks, Bernoulli, Poisson, Normal, Beta, Gamma, their extension in higher dimension or dispersion are introduced. Due to heterogeneity inherent in observation, it is recommended to work with distributions with fat-tail or overdispered such as cauchy, t (from normal), negative-binomial (from poisson). Building block can be used for both prior and likleihood. Missing are log-logistic, and extreme value distributions like generalized Pareto.

### prior
Prior classification include,
- purpose: computation-coherent (e.g. lognormal or inverse gamma which are zero-avoiding), identifiability, regularization (constraint for simple, realistic), penalty for unbiasedness

- diffuseness: 5 ladders of prior (hierarchy), non-negativity, tail, defensive
As problem sizes expands, two trends are noticable: joint and tight priors. They get useful answers more quickly as we use as much information as possible, even solely for computational purpose, but additional care is needed to check assumptions are conherent.

- Sec. 7.3 in workflow [parper](https://arxiv.org/pdf/2011.01808.pdf) introduces prior construction: constrictive prior checks how each module affects the support of the model, structural prior modify parameters w.r.t. partial derivative of some constraint function, computation-coherent prior initialize a simple model, and assume tighter priors if need be, especially for multilevel modules

### likelihood
Casestudies are the best to undersand M. 
- [golf case study](https://mc-stan.org/users/documentation/case-studies/golf.html)
- [birthday](https://github.com/avehtari/casestudies/blob/master/Birthdays/birthdays.html)


# 3. `C` Inference algorithm / Computational model
- [approximate bayesian inference by Moon](https://www.hyunjimoon.com/blog/approximate-bayesian-inference/)
- [probablistic computation alg by Betancourt](https://betanalpha.github.io/assets/case_studies/probabilistic_computation.html#3_probabilistic_computational_algorithms)

# 4. `QI`
- bayesopt
    - reading chapters: Ch. 4,5,6,7,9,10
    - Ch. 4(especially 4.5 ★★★)
    ![](https://i.imgur.com/jtkotNt.png) 
    think objects ~ model

# 5. Simulated data experiment
- [Simulation Intelligence: Towards a New Generation of Scientific Methods](https://arxiv.org/abs/2112.03235)
- [Designing for Interactive Exploratory Data Analysis Requires Theories of Graphical Inference](https://hdsr.mitpress.mit.edu/pub/w075glo6/release/2?readingCollection=c6a3a10e)

