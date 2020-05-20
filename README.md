Covid-19: The case of Spain
================
JMSS \[Usal - CIC\]
(updated: 20 may 2020)

# Models for the COVID-19 pandemic in Spain

## DATA

Daily data: [Datadista
GitHub](https://github.com/datadista/datasets/tree/master/COVID%2019)
(and Ministerio de Sanidad
[MSCBS](https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/situacionActual.htm))

![](README_files/figure-gfm/data%20plots-1.png)<!-- -->![](README_files/figure-gfm/data%20plots-2.png)<!-- -->![](README_files/figure-gfm/data%20plots-3.png)<!-- -->![](README_files/figure-gfm/data%20plots-4.png)<!-- -->

Since we do not know the true data of infected people, two important
variables to take into account are the daily increase in infected and
death people.

![](README_files/figure-gfm/increase%20plot-1.png)<!-- -->![](README_files/figure-gfm/increase%20plot-2.png)<!-- -->

The following graph shows the differences between CC.AA. (regions) in
mortality per 10,000 inhabitants.

![](README_files/figure-gfm/mort-1.png)<!-- -->

-----

## CUBIC SPLINES

Since April 5, I propose this new model to predict the number of deaths
and infecteds, cause the SIR and Regression models seem to make bigger
mistakes in their predictions. Since May 20 the model use as “infecteds”
the number of confirmed only by PCR.

It is based on interpolation with cubic splines. See
[Wikipedia](https://en.wikipedia.org/wiki/Spline_interpolation)

![](README_files/figure-gfm/splinesI-1.png)<!-- -->

![](README_files/figure-gfm/splinesD-1.png)<!-- -->

##### Infecteds forecast for tomorrow (2020-05-21): 233073

##### Deaths forecast for tomorrow (2020-05-21): 27998

Previous predictions:

    Infecteds forecast:

    20-05 -> predicted = 232037; observed = 232555; error = -0.22%

    Deaths forecast:

    06-04 -> predicted = 13092; observed = 12462; error =  4.81%
    07-04 -> predicted = 13692; observed = 13219; error =  3.45%
    08-04 -> predicted = 14541; observed = 13976; error =  3.89%
    09-04 -> predicted = 15312; observed = 14757; error =  3.62%
    10-04 -> predicted = 15921; observed = 15399; error =  3.28%
    11-04 -> predicted = 16448; observed = 15899; error =  3.34%
    12-04 -> predicted = 16863; observed = 16505; error =  2.12%
    13-04 -> predicted = 17591; observed = 17056; error =  3.04%
    14-04 -> predicted = 18006; observed = 17591; error =  2.30%
    15-04 -> predicted = 18623; observed = 18276; error =  1.86%
    16-04 -> predicted = 19102; observed = 18893; error =  1.09%
    17-04 -> predicted = 19681; observed = 19478; error =  1.03%
    18-04 -> predicted = 19826; observed = 20043; error = -1.09%
    19-04 -> predicted = 20608; observed = 20453; error =  0.75%
    20-04 -> predicted = 20863; observed = 20852; error =  0.05%
    21-04 -> predicted = 21251; observed = 21282; error = -0.15%
    22-04 -> predicted = 21712; observed = 21717; error = -0.02%
    23-04 -> predicted = 22152; observed = 22157; error = -0.02%
    24-04 -> predicted = 22597; observed = 22524; error =  0.32%
    25-04 -> predicted = 22891; observed = 22902; error = -0.05%
    26-04 -> predicted = 23280; observed = 23190; error =  0.39%
    27-04 -> predicted = 23478; observed = 23521; error = -0.18%
    28-04 -> predicted = 23852; observed = 23822; error =  0.13%
    29-04 -> predicted = 24123; observed = 24279; error = -0.65%
    30-04 -> predicted = 24728; observed = 24547; error =  0.73%
    01-05 -> predicted = 24811; observed = 24827; error = -0.06%
    02-05 -> predicted = 25105; observed = 25106; error =  0.00%
    03-05 -> predicted = 25376; observed = 25270; error =  0.42%
    04-05 -> predicted = 25428; observed = 25434; error = -0.02%
    05-05 -> predicted = 25592; observed = 25619; error = -0.11%
    06-05 -> predicted = 25798; observed = 25863; error = -0.25%
    07-05 -> predicted = 26101; observed = 26075; error =  0.10%
    08-05 -> predicted = 26283; observed = 26303; error = -0.08%
    09-05 -> predicted = 26528; observed = 26482; error =  0.17%
    10-05 -> predicted = 26657; observed = 26625; error =  0.12%
    11-05 -> predicted = 26764; observed = 26748; error =  0.06%
    12-05 -> predicted = 26867; observed = 26923; error = -0.21%
    13-05 -> predicted = 27096; observed = 27106; error = -0.04%
    14-05 -> predicted = 27288; observed = 27323; error = -0.13%
    15-05 -> predicted = 27538; observed = 27461; error =  0.28%
    16-05 -> predicted = 27597; observed = 27563; error =  0.12%
    17-05 -> predicted = 27667; observed = 27650; error =  0.06%
    18-05 -> predicted = 27737; observed = 27709; error =  0.10%
    19-05 -> predicted = 27768; observed = 27778; error = -0.04%
    20-05 -> predicted = 27847; observed = 27888; error = -0.15%

-----

\#StayAtHome \#QuedateEnCasa
