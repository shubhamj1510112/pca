# PCA
<p align="justify"> This package makes an interactive PCA plot using the gene intensity data for different samples or individuals and also save the plot as a static png file in the working directory. The PCA analysis can be done with or without scaling the data. This option allows revealing the effect of data scaling on PCA analysis. </p>

<p align="justify"> It save the plot as a static ‘png’ file format in the working directory and also generates an interactive PCA plot in the ‘html’ file format which directly opens in the web browser. For static plot “factoextra” library was used and for interactive plot “plotly” library was used. The package also can handle many types of errors such as presence of both intensity and metadata file, files to be in comma separated (.csv) format, existence of the “symbol” column in the intensity file, and same time units for all the samples. The function can also handle the missing values as they may give an error in the PCA analysis. PCA analysis based on singular value decomposition on mean-centered data was performed using the ‘prcomp’ function from “Stats” package. </p>

## Commands to install and run the package

(Start a new R session. Set the working directory as the folder which contains the two input files: intensity file and metadata file. Run following commands)

setwd("path/to/working/directory")

if (!require("devtools")) install.packages("devtools")

require(devtools)

install_github("shubhamj1510112/PCA")

require(PCA)

search()

plotpca_withscaling(genedata="Assignment-gene_data.csv", metadata="Assignment-Meta_data sheet.csv")

plotpca_withoutscaling(genedata="Assignment-gene_data.csv", metadata="Assignment-Meta_data sheet.csv")

(Be patient ! these functions may take up to 2 mins)

