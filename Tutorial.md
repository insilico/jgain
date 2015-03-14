# Tutorial #

### 1. Load and Preprocess Data ###
Load the small sample file provided, called "example\_data.tab," is provided.  In addition to tab delimited, GAIN also accepts arff format.

In the _Pair-wise correlations_ area, select the correlation threshold (.8 by default) and click _Calculate_ then _Show Correlated_ tab.  You may remove redundant SNPs by checking the box next to a SNP and clicking Remove.  A utility is also provided in _Attributes of Interest_ that allows the user to provide a list of SNPs to keep for analysis and remove all others. A file has been created that has a list of SNPs to keep in the data file.  Choose and Apply the "correlation\_filter\_list.txt," which will create a smaller data set of non-redundant SNPs.

### 2. Interaction Analysis ###

Change the _Interaction Lower Bound_ to .03 and Run.  Decrease the lower bound to see other possible interactions not shown by a more strict threshold.  In Interaction Table, click the column labeled _Selected_ to select all SNP pairs then click _Visualize Network_.  You can also select the _Network Degrees_ tab to see the number of connections each node has and the _Export Results_ tab to export results like the network to cytoscape format.

### 3. Permutation Analysis ###

To estimate the interaction threshold to use for the Interaction Lower Bound, click Run in Permutation Analysis.  This will generate the interaction gain scores between 500 randomized pairs then return the threshold for a false connection rate of .05.  The permutation algorithm looks for the randomized score such that 5% of the random scores are more extreme.  This score can be interpreted as 5% of the connections above this threshold are false.