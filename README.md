# [The Dynamic Shift Detector: An algorithm to identify changes in parameter values governing populations](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1007542)

### Christie A. Bahlai [@cbahlai](https://github.com/cbahlai) and Elise F. Zipkin [@ezipkin](https://github.com/ezipkin)

### PLOS Computational Biology

### Please contact the first author for questions about the code or data: Christie Bahlai (cbahlai@kent.edu)
________________________________________________________________________________________________________________________________________
## Abstract:
Environmental factors interact with internal rules of population regulation, sometimes perturbing systems to alternate dynamics though changes in parameter values. Yet, pinpointing when such changes occur in naturally fluctuating populations is difficult. An algorithmic approach that can identify the timing and magnitude of parameter shifts would facilitate understanding of abrupt ecological transitions with potential to inform conservation and management of species. The “Dynamic Shift Detector” is an algorithm to identify changes in parameter values governing temporal fluctuations in populations with nonlinear dynamics. The algorithm examines population time series data for the presence, location, and magnitude of parameter shifts. It uses an iterative approach to fitting subsets of time series data, then ranks the fit of break point combinations using model selection, assigning a relative weight to each break. We examined the performance of the Dynamic Shift Detector with simulations and two case studies. Under low environmental/sampling noise, the break point sets selected by the Dynamic Shift Detector contained the true simulated breaks with 70–100% accuracy. The weighting tool generally assigned breaks intentionally placed in simulated data (i.e., true breaks) with weights averaging >0.8 and those due to sampling error (i.e., erroneous breaks) with weights averaging <0.2. In our case study examining an invasion process, the algorithm identified shifts in population cycling associated with variations in resource availability. The shifts identified for the conservation case study highlight a decline process that generally coincided with changing management practices affecting the availability of hostplant resources. When interpreted in the context of species biology, the Dynamic Shift Detector algorithm can aid management decisions and identify critical time periods related to species’ dynamics. In an era of rapid global change, such tools can provide key insights into the conditions under which population parameters, and their corresponding dynamics, can shift.

## Code

**dynamic_shift_detector.R** - contains functions to detect regime shifts in population time series. The function DSdetector() takes raw time series data and generates a complete report on fits, best fits, break points, and regression parameters for models with best fits

**monarch_example.R** - applies the dynamic shift detector analysis to monarch overwintering data from Mexico

**plot_monarch_figures.R** - plots output from monarch example, places outputs in **figs folder**

**harmonia_example.R** - applies the dynamic shift detector analysis to harmonia ladybeetle population data from Kellogg Biological Station (Includes data cleaning/manipulation code after Bahlai et al 2015)

**plot_harmona_figures.R** - plots output from harmonia example, places outputs in **figs folder**

**simulations.R**- a set of functions that creates time series data using secified parameters, and then a set of funtions to test if the parameters input match the ones detected by the dynamic shift detector, and the code that creates simulations under a variety of conditions, runs it through the comparison functions, and tallies the outputs, outputs a CSV file to the **'simresults' folder**

**plot_simulation_results.R** - takes the simulation outputs and creates plots based on varying one input at a time to see the DSdetector's performance under differing conditions- outputs figures as PDF vector graphis to the **'figs' folder**

## Data

**casestudydata folder** contains data for Harmonia case study. Monarch study data are proprietary

**simresults folder** contains simpulation output CSVs, in sets of one iteration of each case per file

**figs folder** PDF versions of all figs produced be scripts are held in this folder

**tests folder** contains a version of the RSdetector code and test data used in development

**writing folder** contains bits of writing, abstracts, etc, relevant to presentations and publications on this project









<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
