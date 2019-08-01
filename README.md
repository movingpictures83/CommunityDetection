# CommunityDetection
# Language: Python
# Input: CSV (network)
# Output: CSV (dendogram)
# Tested with: PluMA 1.0, Python 3.6

PluMA plugin to perform community detection using the Girvan-Newman method (Girvan and Newman, 2002).

The algorithm forms communities iteratively, using dendograms, by repeatedly removing the edge with
the largest betweenness.

The plugin expects input in the form of a CSV file, where rows and columns each represent nodes
and internal entries the edge weights, i.e. a value A(i, j)=k means that there is an edge from i to j
with weight k.

The plugin will also output a CSV file, with this time the rows representing communities and the columns
representing nodes.  Any nodes with a non-zero value are a member of the community.  For example,
a value A(i, j)=(some nonzero k) means that node j is a member of community i.
