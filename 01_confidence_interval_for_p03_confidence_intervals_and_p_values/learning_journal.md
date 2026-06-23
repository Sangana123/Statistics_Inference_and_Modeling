# Exercise 1 – Confidence Interval for a Proportion

## Objective

Estimate voter support for a candidate using polling data and construct a 95% confidence interval for the population proportion.

## Dataset

* Package: dslabs
* Dataset: polls_us_election_2016

## Statistical Background

A poll provides an estimate of the true proportion of voters supporting a candidate.

Let:

* p̂ = observed sample proportion
* N = sample size

The standard error of the estimate is:

SE(p̂) = sqrt( p̂(1-p̂) / N )

A 95% confidence interval is:

p̂ ± 1.96 × SE(p̂)

## Method

1. Filter polls conducted in the United States.
2. Keep polls ending on or after October 31, 2016.
3. Extract the sample size from the first poll.
4. Convert Clinton support from a percentage to a proportion.
5. Compute the standard error.
6. Construct the 95% confidence interval.

## R Concepts Used

* filter()
* nrow()
* vectors
* sqrt()
* qnorm()

## Key Takeaways

* A confidence interval quantifies uncertainty around a sample estimate.
* Larger sample sizes produce smaller standard errors.
* A 95% confidence interval does not mean there is a 95% probability that the true value lies inside the interval.
* If sampling were repeated many times, approximately 95% of the intervals would contain the true population parameter.


[1] 70
[1] 2220
[1] 0.47
[1] 0.01059279
[1] 0.4492385 0.4907615
  state  startdate    enddate
1  U.S. 2016-11-03 2016-11-06
2  U.S. 2016-11-01 2016-11-07
3  U.S. 2016-11-02 2016-11-06
4  U.S. 2016-11-04 2016-11-07
5  U.S. 2016-11-03 2016-11-06
6  U.S. 2016-11-03 2016-11-06
                                                    pollster grade samplesize
1                                   ABC News/Washington Post    A+       2220
2                                    Google Consumer Surveys     B      26574
3                                                      Ipsos    A-       2195
4                                                     YouGov     B       3677
5                                           Gravis Marketing    B-      16639
6 Fox News/Anderson Robbins Research/Shaw & Company Research     A       1295
  population rawpoll_clinton rawpoll_trump rawpoll_johnson rawpoll_mcmullin
1         lv           47.00         43.00            4.00               NA
2         lv           38.03         35.69            5.46               NA
3         lv           42.00         39.00            6.00               NA
4         lv           45.00         41.00            5.00               NA
5         rv           47.00         43.00            3.00               NA
6         lv           48.00         44.00            3.00               NA
  adjpoll_clinton adjpoll_trump adjpoll_johnson adjpoll_mcmullin
1        45.20163      41.72430        4.626221               NA
2        43.34557      41.21439        5.175792               NA
3        42.02638      38.81620        6.844734               NA
4        45.65676      40.92004        6.069454               NA
5        46.84089      42.33184        3.726098               NA
6        49.02208      43.95631        3.057876               NA