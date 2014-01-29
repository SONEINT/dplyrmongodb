dplyrmongodb
============

This is an R (www.r-project.org) package providing a grammar of data manipulation on MongoDB (www.mongodb.org) motivated by the plyr & dplyr packages. dplyr (https://github.com/hadley/dplyr) is the next iteration of plyr (https://github.com/hadley/plyr), focused on tools for working with data frames no matter where it's stored, whether in a data frame, a data table or database. The package **dplyrmongodb** provides a very similar functionality and syntax in R for data stored in MongoDB.


There is no stable CRAN version available so far.


Please feel free to send us issues or pull requests via github: https://github.com/schmidb/dplyrmongodb

Furthermore, we are happy to get your feedback personally via email: markus@mongosoup.de



Usage
==================
Once you have installed the package, it may be loaded from within R like any other package:

    library("dplyrmongodb")
    
    # connect to your local mongodb
    mongo <- mongo.create()
    
    # ToDo
    
    mongo.disconnect(mongo)
    mongo.destroy(mongo)




### Supported Functionality by dplyrmongodb
* ToDo


### Good ressources to Get Started with plyr or dplyr
* ToDo



Development
==================

To install the development version of rmongodb, it's easiest to use the devtools package:

    # install.packages("devtools")
    library(devtools)
    install_github("dplyrmongodb", "schmidb")
    
We advice using RStudio (www.rstudio.org) for the package development. The RStudio .Rproj file is included in the repository.

### Versioning
We use a three step version number system, e.g. v1.2.1:
* first: major changes
* second: for each new stable CRAN release
* third: for each new github version ready for testing

### General Development Rules
* we use roxygen2
* we write RUnit tests for all new functionality in tests/test_XXX.R
* for bigger changes we use branches
* CRAN submission:
 * http://cran.r-project.org/submit.html
 * create Package tar.gz via RStudio "Build Source Package"
 * run CRAN checks via: R CMD check --as-cran package.tar.gz
 * create a tag / release on github for every CRAN submission