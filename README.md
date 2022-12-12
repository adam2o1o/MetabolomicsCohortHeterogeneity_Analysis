<a name="readme-top"></a>


<!-- PROJECT LOGO -->
<br />
<div align="center">
  <h1 align="center">Code for "Overcoming cohort heterogeneity for the prediction of subclinical cardiovascular disease risk"</h1>
</div>


## About

The code for this project was compiled in *R* language using *RMarkdown*


<!-- GETTING STARTED -->
## Getting Started

To reproduce the analysis, clone all the files in the repository. In RStudio, set the root folder as the working directory and compile (Knit) the `MetabolomicsCohortHeterogeneity.Rmd` file. 

To view the analysis, open the `MetabolomicsCohortHeterogeneity.html` file which contains the code and figures used in the manuscript. 

## File Information

Raw Data:
* `data_raw\BioHEART_cohort_heterogeneity_clin_data.csv` - Table containing patient clinical/demographic information
* `data_raw\BioHEART_metabolomics.csv` - Table containing processed metabolomics data used for analysis. Metabolomics data processed as described in [hRUV: A hierarchical approach to removal of unwanted variation for large-scale metabolomics data](https://www.nature.com/articles/s41467-021-25210-5).

Processed Data:
* `data_processed\BioHEART_metabolomics_hRUV_AC.rds` - hRUV normalised metabolomics data. Processed metabolomics data was log2 transformed, and then metabolites with over 25% missing were removed. Missing values were imputed with minimum value, and then hRUV was applied with the parameters: intra = "loessShort", inter = "concatenate", intra_k = 15, inter_k = 3.
* `data_processed\mtb_hruv_std_ratio_cv_subgroup_res.RData` - Cross validation results from modelling within each subgroup
* `data_processed\mtb_hruv_std_ratio_rmoe_model_l1_0.012_l2_0.08.RData` - Regularized Mixture of Experts output from the NEMoE R package, using lambda1 = 0.012, lambda2=0.08, init="kmeans", K=2
* `data_processed\mtb_hruv_std_ratio_t_test_df.RData` - test statistics from t-tests of each metabolite ratio within each subgroup


<!-- CONTACT -->
## Contact

Adam Chan - [adam2o1o](https://github.com/adam2o1o) - adam.s.chan@sydney.edu.au

Manuscript Link: [Currently under review]()

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[rmarkdown-logo-url]: https://community.rstudio.com/uploads/default/optimized/3X/8/6/868106552b1bf0f370328768e53e562d1c659ffd_2_432x498.png