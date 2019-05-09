# Mapping Early American Elections

This repository contains the data from the *[Mapping Early American Elections](http://earlyamericanelections.org/)* project at the [Roy Rosenzweig Center for History and New Media](http://rrchnm.org/). This project, which is funded by the Division of Preservation and Access at the National Endowment for the Humanities, is based on the data from the *[New Nation Votes](http://elections.lib.tufts.edu/)* project. 

## Tutorials

For more information about how to use this dataset, please see our tutorials:

- [Tutorial for R](http://earlyamericanelections.org/blog/2019/04/30/r-tutorial.html)
- [Tutorial for QGIS](http://earlyamericanelections.org/blog/2019/04/30/qgis-tutorial.html)

## Relationship to datasets

This dataset has been prepared for use with several spatial datasets. Please see the citations for and links to those datasets on [our website's data page](http://earlyamericanelections.org/data/). These are the datasets:

-   John H. Long and Peggy Tuck Sinko, *[Atlas of Historical County Boundaries](http://publications.newberry.org/ahcbp/)*, Dr. William M. Scholl Center for American History and Culture, Newberry Library (2010).
-   Jeffrey B. Lewis, Brandon DeVine, Lincoln Pitcher, and Kenneth C. Martis, *[Digital Boundary Definitions of United States Congressional Districts, 1789--2012](http://cdmaps.polisci.ucla.edu)*, University of California, Los Angels (2013).
-   Erik Steiner, *[United States Historical City Populations, 1790--2010](https://github.com/cestastanford/historical-us-city-populations)*, Spatial History Project, Center for Spatial and Textual Analysis, Stanford University (2015).

This repository also contains information and IDs from the [Biographical Directory of the United States Congress](http://bioguide.congress.gov/biosearch/biosearch.asp).

## Repository structure

Most of the CSV files in this dataset are intended to work together like the tables in a relational database. But many of the files are also intended for your convenience in mapping. Below is a description of the most significant files and directories.

CSV files:

- `candidates.csv`. All of the candidates in the NNV dataset, with additional information from the Congressional Biographical Directory where available.
- `congbio_elected.csv`. A list of who was elected in Congressional elections, according to the Congresional Biographical Directory.
- `congressional-candidate-totals.csv`. The total votes for each candidate in Congressional elections.
- `congressional-counties-parties.csv`. The total votes for each party by county in a Congressional election. This data can be mapped by county using the AHCB county data.
- `congressional-elections-dates.csv`. The best approximation of which date to use for each of the state Congressional elections.
- ` elections.csv`. The elections (i.e., ballots) listed in the NNV dataset that pertain to Congressional elections.
- `maps-to-elections.csv`. Each ID from the Mapping Elections project gathers together the ballots from NNV into a map of all Congressional elections happening in that state.
- `maps.csv`. Contains an ID for each map created by the Mapping Elections project, which can be used with `maps-to-elections.csv` to gather the election returns from NNV.
- `staterepresentative-candidate-totals.csv`. The total votes for each candidate in selected elections for state representatives.
- `staterepresentative-counties-parties.csv`. The total votes for each party by county in a selected elections for state representatives. This data can be mapped by county using the AHCB county data.

Directories:

- `congressional-parties-by-state/`. This directory contains the data in `congressional-counties-parties.csv`, but split apart into one file per state and Congress identified by MEAE ID. This format may be more convenient for mapping in GIS and other software.
- `congressional-candidates-by-state/`. This directory contains the data in `congressional-candidate-totals.csv`, but split apart into one file per state and Congress identified by MEAE ID. This format may be more convenient for mapping in GIS and other software.
- `towns/`. This directory contains latitutes and longitudes from the states that reported significant numbers of election returns by town in the NNV dataset.

## License

The data in this repository from *Mapping Early American Elections* is made available under the Open Data Commons Attribution License, [ODC-BY 1.0](http://opendatacommons.org/licenses/by/summary/). The data is derived and modified from the NNV data, which is licensed under a Creative Commons Zero ([CC0](http://elections.lib.tufts.edu/terms.html)) dedication.

