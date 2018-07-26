# This is a set of scripts that we use in our [group of plant proteomics](http://plantprot.lab/) for certain routine tasks 
### PeptideCutterParser.py
__Description__: This script is useful for overlapping the protease sites cleavage and sites of MS peptide origins. 
	It require Internet connection and that protein ids are recognizable by [Expasy PeptideCutter](https://web.expasy.org/peptide_cutter/) which is used to determine the cleavage sites.

__Usage__: python3 PeptideCutterParser.py table

	table - a tab separated table with first two columns are (!no header!):
	1. Protein ID (!recognizable by Expasy PeptideCutter)
	2. Sites for MS peptide origin (e.g. 23-35).
__Example__:

A9SNP9	118-127

A9U4B4	118-127

A0A2K1IE22	1-10, 77-86

### Output:

Table with first following columns: 

1. protein_id 

2. Names of enzymes overlapping START position of MS peptide

3. Names of enzymes overlapping END position of MS peptide
