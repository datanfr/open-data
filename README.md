
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Open Data - DATAN

Ce repo contient certaines données publiques utilisées par le site de
vulgarisation parlementaire
[Datan](https://www.resultats-elections.interieur.gouv.fr/legislatives-2022/index.html).

## Élections législatives

Les fichiers contiennent les données pour les élections législatives
françaises suivantes : 2017, 2022 et 2024.

Ces données sont issues des données publiques du ministère de
l’Intérieur [publiées sur le site Data
Gouv](https://www.data.gouv.fr/fr/pages/donnees-des-elections/).

- *circo_infos.rds*

Ce jeu de données contient les informations électorales concernant les
circonscriptions.

``` r
dplyr::glimpse(readr::read_rds("elections/legislatives/circo_infos.rds"))
#> Rows: 2,227
#> Columns: 12
#> $ dpt         <chr> "01", "01", "01", "01", "01", "02", "02", "02", "02", "02"…
#> $ dpt_url     <chr> "001", "001", "001", "001", "001", "002", "002", "002", "0…
#> $ circo       <int> 1, 2, 3, 4, 5, 1, 2, 3, 4, 5, 1, 2, 3, 1, 2, 1, 2, 1, 2, 3…
#> $ circo_url   <int> 1, 2, 3, 4, 5, 1, 2, 3, 4, 5, 1, 2, 3, 1, 2, 1, 2, 1, 2, 3…
#> $ tour        <int> 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2…
#> $ inscrits    <int> 82673, 93507, 75548, 89382, 75289, 72347, 73976, 68085, 79…
#> $ abstentions <int> 46945, 54341, 46438, 51079, 43569, 39583, 42321, 36747, 47…
#> $ votants     <int> 35728, 39166, 29110, 38303, 31720, 32764, 31655, 31338, 32…
#> $ blancs      <int> 2245, 2424, 1815, 2670, 2050, 2262, 1672, 1606, 2192, 2253…
#> $ nuls        <int> 805, 867, 539, 697, 749, 824, 709, 687, 952, 817, 1356, 20…
#> $ exprimes    <int> 32678, 35875, 26756, 34936, 28921, 29678, 29274, 29045, 28…
#> $ year        <int> 2017, 2017, 2017, 2017, 2017, 2017, 2017, 2017, 2017, 2017…
```

- *circo_results.rds*

Ce jeu de données contient les résultats par circonscription.

``` r
dplyr::glimpse(readr::read_rds("elections/legislatives/circo_results.rds"))
#> Rows: 7,442
#> Columns: 15
#> $ year         <int> 2017, 2017, 2017, 2017, 2017, 2017, 2017, 2017, 2017, 201…
#> $ dpt          <chr> "01", "01", "01", "01", "01", "01", "01", "01", "01", "01…
#> $ dpt_url      <chr> "001", "001", "001", "001", "001", "001", "001", "001", "…
#> $ circo        <int> 1, 1, 2, 2, 3, 3, 4, 4, 5, 5, 1, 1, 2, 2, 3, 3, 4, 4, 5, …
#> $ circo_url    <int> 1, 1, 2, 2, 3, 3, 4, 4, 5, 5, 1, 1, 2, 2, 3, 3, 4, 4, 5, …
#> $ tour         <int> 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, …
#> $ nuance       <chr> "LR", "MDM", "LR", "MDM", "REM", "LR", "REM", "FN", "LR",…
#> $ candidat     <chr> "M. Xavier BRETON", "M. Laurent MALLET", "M. Charles DE L…
#> $ nameLast     <chr> "NULL", "NULL", "NULL", "NULL", "NULL", "NULL", "NULL", "…
#> $ nameFirst    <chr> "NULL", "NULL", "NULL", "NULL", "NULL", "NULL", "NULL", "…
#> $ sexe         <chr> "NULL", "NULL", "NULL", "NULL", "NULL", "NULL", "NULL", "…
#> $ voix         <int> 17564, 15114, 18556, 17319, 16552, 10204, 22532, 12404, 1…
#> $ pct_inscrits <dbl> 21.25, 18.28, 19.84, 18.52, 21.91, 13.51, 25.21, 13.88, 2…
#> $ pct_exprimes <dbl> 53.75, 46.25, 51.72, 48.28, 61.86, 38.14, 64.50, 35.50, 6…
#> $ elected      <int> 1, 0, 1, 0, 1, 0, 1, 0, 1, 0, 1, 0, 1, 0, 1, 0, 1, 0, 1, …
```

- *cities.rds*

Ce jeu de données contient les résultats par commune.

``` r
dplyr::glimpse(readr::read_rds("elections/legislatives/cities.rds"))
#> Rows: 431,417
#> Columns: 18
#> $ year      <int> 2017, 2017, 2017, 2017, 2017, 2017, 2017, 2017, 2017, 2017, …
#> $ tour      <int> 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, …
#> $ dpt       <chr> "01", "01", "01", "01", "01", "01", "01", "01", "01", "01", …
#> $ circo     <chr> "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", "1", …
#> $ commune   <int> 16, 16, 24, 24, 29, 29, 38, 38, 40, 40, 50, 50, 53, 53, 57, …
#> $ insee     <chr> "01016", "01016", "01024", "01024", "01029", "01029", "01038…
#> $ inscrits  <int> 317, 317, 2325, 2325, 429, 429, 575, 575, 346, 346, 248, 248…
#> $ abs       <int> 167, 167, 1342, 1342, 252, 252, 295, 295, 210, 210, 153, 153…
#> $ votants   <int> 150, 150, 983, 983, 177, 177, 280, 280, 136, 136, 95, 95, 61…
#> $ blancs    <int> 13, 13, 57, 57, 8, 8, 20, 20, 7, 7, 4, 4, 436, 436, 21, 21, …
#> $ nuls      <int> 3, 3, 16, 16, 10, 10, 3, 3, 4, 4, 2, 2, 118, 118, 3, 3, 11, …
#> $ exprimes  <int> 134, 134, 910, 910, 159, 159, 257, 257, 125, 125, 89, 89, 55…
#> $ candidate <chr> "c_1", "c_2", "c_1", "c_2", "c_1", "c_2", "c_1", "c_2", "c_1…
#> $ sexe      <chr> "M", "M", "M", "M", "M", "M", "M", "M", "M", "M", "M", "M", …
#> $ nom       <chr> "BRETON", "MALLET", "BRETON", "MALLET", "BRETON", "MALLET", …
#> $ prenom    <chr> "Xavier", "Laurent", "Xavier", "Laurent", "Xavier", "Laurent…
#> $ nuance    <chr> "LR", "MDM", "LR", "MDM", "LR", "MDM", "LR", "MDM", "LR", "M…
#> $ voix      <int> 84, 50, 486, 424, 91, 68, 146, 111, 76, 49, 57, 32, 2915, 26…
```
