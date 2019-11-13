# shinyPred

This is a shiny app to analyse the impact of chemical treatments on a growing vole population

## Import trapping plan file

A chemical treatment file is just a text file tab delimited with two headed columns like the following:


```
Day	Efficiency
2	0.8
30	0.8
90	0.8
120	0.8

```

This means that a treatment is achieved on days 2, 30, 90, 120 and that 80% of the voles were killed each day.

An empty file such as below can be uploaded to set trapping effort to zero (until I find a clean way to do it otherwise...)

```
Day	Efficiency
1	0
```


## Caveats

- There are few controls at this stage. It is therefore advisable not to plan trapping day 1 (the day where the initial values of the population is given; population starts day 2; treatment day 1 would not be taken into account), or any day > 360 (which exceeds the time limit).

-  Non intentional effects of treatments, e.g. the impact of treatments on predators is not taken into account (hence supposed to be zero).


## Ecology

- The number of predators is constant;
- Non intentional effects of treatments, e.g. the impact of treatments on predators is not taken into account (hence supposed to be zero).
- The functional response is of the Holling II type (in short, the variation in the proportion of voles in the diet saturates at 100% with high densities of voles);
- The intrinsic rate of voles (r0) population growth means that one vole female produces, by embedded generations, potentially 100 voles (50 females) during a breeding season;
- The growth is logistic, and the biotic capacity is fixed to the maximum number of voles that the environment can support;
- The breeding season starts on March 1 and lasts 8 months (8 x 30 days), then for 4 months (4 x 30 days) the breeding stops (no other mortality other than that due to predation is taken into account during this period).


