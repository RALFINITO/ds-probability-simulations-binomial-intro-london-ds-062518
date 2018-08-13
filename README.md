
## Probability with Simulations


```python
import numpy as np 
import matplotlib.pylab as plt
%matplotlib inline
```

### Simple probabilities

We can use numpy's [random.choice](https://docs.scipy.org/doc/numpy/reference/generated/numpy.random.choice.html) function to take samples from a defined sample space and estimate probability. 

For a fair coin we have to states:

Simulate coin flips with the random choice function.

Try to simulate many flips of the coin and store the results in an array by passing the `size` parameter to `np.random.choice`



Now suppose we want to run a simple simulation to estimate the probability that the coin comes up Heads (which we expect to be .5 because the coin is fair). One way to do this is to do a large number of coin flips and then divide the number of flips that come up Heads by the total number of flips. Flip the coin 50 times and compute the results

Let's see what happens if we rerun the simulation with an increasing number of coin flips.

It's an interesting exercise to make a plot of the running estimate of the probability as the number of coin flips increases. We'll use the same random sequence of coin flips from the previous simulation.



### The Binomial Distribution

A binomial distribution can be thought of as simply the probability of a SUCCESS or FAILURE outcome in an experiment or survey that is repeated multiple times. The binomial is a type of distribution that has two possible outcomes (the prefix “bi” means two, or twice). For example, a coin toss has only two possible outcomes: heads or tails and taking a test could have two possible outcomes: pass or fail.

The binomial is defined by two parameters: the probability of success in any given trial and the number of trials. The binomial distribution tells you how likely it is to achieve a given number of successes in n trials of the experiment. 

For example, we could model flipping a fair coin 10 times with a binomial distribution where the number of trials is set to 10 and the probability of success is set to 0.5. In this case the distribution would tell us how likely it is to get zero heads, 1 head, 2 heads and so on.

Python's Scipy library has a built in function for calculating binomial distributions called `binom`.


```python
import pandas as pd
import scipy.stats  as stats
```

Lets try to run above with a biased coin

## Uniform distribution

The uniform distribution is a probability distribution where each value within a certain range is equally likely to occur and values outside of the range never occur. If we make a density plot of a uniform distribution, it appears flat because no value is any more likely (and hence has any more density) than another.
This distribution is defined by two parameters, a and b:

a is the minimum.
b is the maximum.
The distribution is written as U(a,b).

Many useful functions for working with probability distributions in Python are contained in the scipy.stats library. 

* 100000 data points 
* range: 0 - 10 

The density of our uniform data is essentially level meaning any given value has the same probability of occurring. The area under a probability density curve is always equal to 1.
