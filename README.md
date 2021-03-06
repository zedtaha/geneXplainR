[![Build Status](https://travis-ci.org/genexplain/geneXplainR.svg?branch=master)](https://travis-ci.org/genexplain/geneXplainR)
[![codecov](https://codecov.io/gh/genexplain/geneXplainR/branch/master/graph/badge.svg)](https://codecov.io/gh/genexplain/geneXplainR)
[![status](http://joss.theoj.org/papers/f9e01bf1a9649a3ab078215c81bb6f12/status.svg)](http://joss.theoj.org/papers/f9e01bf1a9649a3ab078215c81bb6f12)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1013318.svg)](https://doi.org/10.5281/zenodo.1013318)

# geneXplainR

The geneXplainR package provides an R client for the 
[geneXplain platform](http://genexplain.com/genexplain-platform/) [1]. 
The geneXplain platform is an online toolbox and workflow management 
system for a broad range of bioinformatic and systems biology applications.
The platform is well-known for its upstream analysis [2], that has been
developed to identify causal signalling molecules on the basis of experimental data
like expression measurements.

geneXplainR is based on and extends the [rbiouml](https://cran.r-project.org/package=rbiouml) package.
A goal of this project is to add functionality that helps to make building R pipelines that use the geneXplain platform easier.

# Installation

## From github.com

The geneXplainR package can be easily installed from its github repository using *devtools*.

```R
library(devtools)
install_github("genexplain/geneXplainR")
```

We hope to make geneXplainR available through other channels as well, so that there will be further options
to download and install the software. 

# Usage

A script using geneXplain may look like this (please note that shown parameters won't work):

```R
library(geneXplainR)
gx.login("https://platform.genexplain.com","user","password")

# Get a listing of your research projects
gx.ls("data/Projects")
```

Login to a personal platform workspace requires valid user name and password which can be obtained for free on the
[geneXplain website](http://genexplain.com/genexplain-platform-registration/).
If you just wish to try out the functionality of geneXplainR, you can sign into the demo account on our
public server *platform.genexplain.com* by simply calling *gx.login()*, without parameters. To access another server that
provides a demo workspace, you can call *gx.login* with the server URL as only argument.

# Documentation and examples

For information about geneXplainR, please refer to the vignettes that come with this package. Furthermore, the *examples* branch of this repository contains a number of examples.

# Support

If you find an issue, we would be happy if you let us know either by writing an e-mail
to [geneXplain](mailto:info@genexplain.com?subject=geneXplainR%20issue) or to the [GitHub issue system](https://github.com/genexplain/geneXplainR/issues).

# References

1. Kel, A., Kolpakov, F., Poroikov, V., Selivanova, G. (2011) GeneXplain — Identification of Causal Biomarkers and Drug Targets in Personalized Cancer Pathways. J. Biomol. Tech. 22(suppl.), S1
2. Koschmann, J., Bhar, A., Stegmaier,P., Kel, A. E. and Wingender, E. (2015) “Upstream Analysis”: An integrated promoter-pathway analysis approach to causal interpretation of microarray data. Microarrays 4, 270-286.
