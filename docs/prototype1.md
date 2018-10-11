## Prototype 1: Voltage follower and anti-alias filter

![prototype1.JPG](../images/prototype1.JPG)

Modifications to Emon2 example:

- Addition of voltage follower on PA6 & PA7
- HAL_OPAMP_Start(&hopamp2); required

Anti-alias filter based on: 

![antialias.png](../images/antialias.png)

Two 1k resistors + 22pF capacitors to ground, biased with output from voltage follower.

Serial output (toaster):

    235.86  0.053   1.2     12.4    0.097   65380
    235.71  0.053   1.2     12.5    0.093   65383
    235.68  0.053   1.3     12.5    0.101   65390
    235.53  0.052   1.2     12.3    0.101   65402
    235.70  0.053   1.1     12.5    0.087   65424
    234.46  3.778   657.2   885.8   0.742   65435
    233.47  4.913   1144.2  1147.1  0.998   65448
    233.48  4.827   1124.3  1127.0  0.998   65468
    233.52  4.800   1118.0  1120.8  0.998   65467
    233.49  4.784   1114.2  1117.0  0.998   65467
    233.44  4.772   1111.3  1114.0  0.998   65475
    233.19  4.759   1107.0  1109.7  0.998   65476
    233.30  4.754   1106.4  1109.1  0.998   65480
    235.58  0.910   42.1    214.4   0.196   65474
    235.47  0.047   1.4     11.1    0.128   65465
    235.61  0.047   1.3     11.0    0.120   65452
    235.62  0.046   1.3     10.9    0.124   65458
    235.44  0.046   1.2     10.9    0.114   65464
    235.58  0.047   1.3     11.0    0.119   65467

40W incandescent lightbulb:

    225.69  0.045   0.5     10.1    0.051   65367
    225.20  0.045   0.5     10.1    0.050   65374
    225.65  0.046   0.5     10.4    0.052   65380
    225.37  0.046   0.5     10.3    0.048   65378
    225.86  0.046   0.5     10.4    0.045   65379
    225.60  0.047   0.5     10.7    0.048   65381
    225.80  0.105   9.7     23.7    0.411   65395
    225.35  0.182   39.4    41.0    0.960   65413
    225.55  0.182   39.3    40.9    0.960   65427
    225.22  0.181   39.2    40.8    0.961   65434
    225.66  0.182   39.4    41.0    0.960   65430
    225.27  0.181   39.2    40.8    0.960   65433
    225.66  0.181   39.3    40.9    0.960   65428
    225.19  0.181   39.2    40.8    0.960   65433
    225.60  0.181   39.3    40.9    0.961   65431
    225.15  0.179   39.1    40.4    0.967   65429
    
22pF filter cap on CT input:

![22pfCT.png](../images/DS/22pfCT.png)

100pF filter cap on CT input:

![100pfCT.png](../images/DS/100pfCT.png)

No filter cap on CT input:

![nocapCT.png](../images/DS/nocapCT.png)

100pF filter cap on Voltage input (22pF on other screenshots), showing to low cut off frequency:

![100pfV.png](../images/DS/100pfV.png)
