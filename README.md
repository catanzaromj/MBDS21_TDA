# A practical introduction to Topological Data Analysis 

A repository for a tutorial on Topological Data Analysis (TDA) for the Midwest
Big Data Summer School in 2021 virtually in Ames, Iowa.

This tutorial covers persistent homology and mapper, 
two of the main tools used in TDA.   

The slides for this tutorial can be found [here]().

## Persistent Homology
For persistent homology, we use two implementation namely [`scikit-tda`](https://scikit-tda.org)
and [`giotto-tda`](https://giotto-ai.github.io/gtda-docs/0.4.0/library.html). 
Both of these packages are available on pypi and everything
you need for the topological data analysis part of the tutorial can be 
installed with
```{python}
   pip install scikit-tda, giotto-tda
```
The tutorial depends on other libraries like `numpy` which I assume you already
have installed.

Both `scikit-tda` and `giotto-tda` implement Vietoris-Rips persistent homology based on the
[Ripser](https://github.com/Ripser/ripser) algorithm, a
very efficient C++ implementation of persistence.
If you don't want to install anything on your computer, you can go to
[live.ripser.org](https://live.ripser.org) and upload the data sets there
for easy persistence computations.

There are three persistent homology notebooks for users to work through:
1. [Introduction to persistent homology](Intro_to_PH.ipynb). A simple notebook with mostly synthetic data sets to work through.
2. [Differentiation using persistence landscapes](Differentiation_with_Persistence_Landscapes.ipynb). A notebook for distinguishing $S^2$ from $S^3$ using one-dimensional homology, highlighting the geometric aspects of persistence. This relies on persistence landscapes, one of the first vectorization schemes introduced for persistence diagrams.
3. [MNIST using persistent homology](MNIST_using_PH.ipynb). The most advanced notebook, combining various cubical persistence with various vectorization schemes to build a digit classifier.

## Mapper
We use [KeplerMapper](https://github.com/scikit-tda/kepler-mapper) 
for our mapper implementation. Kepler Mapper is written in python, and is compatible with other machine learning packages,
like [scikit-learn](https://scikit-learn.org/stable/).

There is one mapper notebook for users to work through: [Introduction to mapper](). An elementary notebook with basic data sets to get accustomed to choosing filter functions, cover parameters, etc.

### Other tutorials
There are a variety of excellent and much more thorough tutorials available
online by experts in the field. Some of the data sets in this tutorial
are either motivated by or come directly from the following:

* [Charleston-TDA-ML](https://github.com/henryadams/Charleston-TDA-ML/wiki).
A tutorial on Persistent Homology written by Henry Adams, 
Melissa McGuirl, and Yitzchak Solomon.

* [Peter Bubenik's TDA with R worksheet](https://people.clas.ufl.edu/peterbubenik/intro-to-tda/). A tutorial on using R to analyze data with Persistence Landscapes.

* [MAA-NCS18](https://github.com/MatthewZabka/MAA-NCS18). Matt Zabka's 
Persistence Homology tutorial.

* [R-TDA tutorial](http://www.stat.cmu.edu/topstat/topstat_old/Talks/files/Jisu_150623_TDA_tutorial.pdf). An R-TDA worksheet tutorial written by Jisu Kim.

* Scikit-tda tutorials: [Ripser.py tutorials](https://ripser.scikit-tda.org/en/latest/), [KeplerMapper tutorials](https://kepler-mapper.scikit-tda.org/en/latest/), [Persim tutorials](https://persim.scikit-tda.org/en/latest/).

* [giotto-tda tutorials](https://giotto-ai.github.io/gtda-docs/0.4.0/notebooks/index.html). A list of tutorials and examples highlighting the functionality of `giotto-tda`.

This list is nowhere near complete, and there are lots of other great tutorials for learning TDA.
