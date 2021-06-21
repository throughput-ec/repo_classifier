[![lifecycle](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)
[![NSF-1928366](https://img.shields.io/badge/NSF-1928366-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1928366)

# Repository Classifier

Pipeline to find out what kind of resource a Code Repository linked to Throughput is:
- educational
- miscellaneous
- software development
- storage


## Contributors

This project is an open project, and contributions are welcome from any individual.  All contributors to this project are bound by a [code of conduct](CODE_OF_CONDUCT.md).  Please review and follow this code of conduct as part of your contribution.

  * [Simon Goring](http://www.goring.org/) [![orcid](https://img.shields.io/badge/orcid-0000--0002--2700--4605-brightgreen.svg)](https://orcid.org/0000-0002-2700-4605)
  * [Socorro Dominguez Vidana](https://sedv8808.github.io/) [![orcid](https://img.shields.io/badge/orcid-0000--0002--7926--4935-brightgreen.svg)](https://orcid.org/0000-0002-7926-4935)


### Tips for Contributing

Issues and bug reports are always welcome.  Code clean-up, and feature additions can be done either through branches.

All products of the Throughput Annotation Project are licensed under an [MIT License](LICENSE) unless otherwise noted.

## How to use this repository

For now, the repository contains 3 notebooks to outline the process.

The first notebook is to get the Repositories ReadMe files. This is done using Neo4j to identify the repositories in Throughtput and then using GitHub's API with a Developer Key.

Content from ReadMe files is encoded in base64 so, decoding is also necessary for our NLP procedures.

### Workflow Overview

This project uses the Throughput Graph Database as an input from neo4j:
* `neotoma:` tsv file

These files are used as input that will help create a Recommender System.
* Predict whether a code repository is educational, misc, etc..

### System Requirements

This project is developed using Python and Neo4j.  
This project will need Neo4j installed.
It runs on a MacOS system.
Continuous integration uses TravisCI.

### Data Requirements

The project pulls data from the Throughput database.
Need a GitHub API secret
Labels were currently given by Morgan Wofford but should be able to get these from annotations in the Throughtput DB in the near future.


### Key Outputs

This project will generate a structured dataset that provides the following information:
* Whether a CR belongs to a certain class.

Currently, the model's accuracy is very poor due to low quantity of labeled data.
However, test performance at its best is 66% (it is still painfully overfitting)

## Pipeline
TODO:
\n
\n

[include workflow chart]

### Instructions
