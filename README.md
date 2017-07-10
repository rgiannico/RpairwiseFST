# RpairwiseFST

### Aim: 
Pairwise FST by population table and plot starting from vcf file

### Needs: 

- R
- "SNPRelate" Rpackage (bioconductor)
- VCF input file
- Population metadata tab separated text input file ('samples' and 'pop' columns required). Here an example:

| samples       | pop     | 
|:------------- |:-------:|
| Sample_1      | BIS |
| Sample_2      | BIS |
| Sample_3      | CEL |
| Sample_4      | CEL |
| Sample_5      | CHM |
| Sample_6      | CHM |

### Example of results: 
- Pairwise FST matrix example:


|        | BIS     | CEL | CHM |
|:--:|:---------:|:--:|:--:|
| **BIS**| 0|0.15 |0.22|
| **CEL**| 0.15|0 |0.26|
| **CHM**| 0.22|0.26 |0|

> This is an example of paiwise FST table with invented values just to match the example metadata table above and the Arlequin's plot below

- Arlequin's plot example:

<img src="https://www.researchgate.net/profile/Vincenzo_Landi/publication/239065621/figure/fig1/AS:216493619978265@1428627509650/Graphic-representation-of-the-matrix-depicting-pairwise-FST-distances-among-the-17-pig.png" width="400">

> This plot is an example of a pairwise FSTplot from [Gama et. al. 2013](https://gsejournal.biomedcentral.com/articles/10.1186/1297-9686-45-18) paper. The Arlequin's pairFstMatrix.r function used here produces this kind of output. 

### Notes: 
- **FST calculation**  is performed using "SNPRelate" bioconductor  Rpackage
- **Pairwise FST matrix PLOT** : is performed using Arlequin's pairFstMatrix.r (Author: Heidi Lischer) with very few edits 
- **Negative Fst** are technical artifact of the computation (see [Roesti el al. 2012](https://bmcevolbiol.biomedcentral.com/articles/10.1186/1471-2148-12-94)) and are automatically replaced with zero.

**Author:** Riccardo Giannico - **Date:** 2017
