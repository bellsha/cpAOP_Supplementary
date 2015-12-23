# cpAOP_Supplementary
Supplementary data for cpAOP paper

**TGGATESProc**
*descretized data files from TG-GATES*

LiverLabDescData201411.txt: Descretized laboratory values for rat coming from https://github.com/bellsha/TGGATESProc/blob/master/TGGATESlabprep.R

PathEnrichReactomeDataFrame.txt: Descretized differentially expressed pathways based on Reactome annotation coming from https://github.com/bellsha/cpAOP/blob/master/gene2biospace.R

open_tggates_pathologyDESC.txt: Descretized liver pathology values for the rats coming from https://github.com/bellsha/TGGATESProc/blob/master/TGGATESpathologyprep.R

*files needed to run code*
RunInfo-Liver-NetRun1501.txt: description of all the data files, columns are: "runID", "fileName","SPECIES","ORGAN_ID", "CHEMICAL", "DOSE_LEVEL", "SACRIFICE_PERIOD","TEST-TYPE","SINGLE_REPEAT_TYPE"

Chem2MechMapping1013.txt: a chemical mapping file that was used to try and group some of the chemicals by mechanism. Used DrugMatrix annotations. Code not provided here

LiverLabChemEdged201411.txt: Values for the chemcial treatment -> clinical chemistry scores coming from https://github.com/bellsha/TGGATESProc/blob/master/TGGATESlabprep.R

LiverPathologyChemicalEdges201411.txt: Values for the chemical treatment -> pathology scores coming from https://github.com/bellsha/TGGATESProc/blob/master/TGGATESpathologyprep.R

PathEnrichReactomeAnnoTable.txt: the annotation table with the treatments and the DE reactome nodes generated in https://github.com/bellsha/cpAOP/blob/master/gene2biospace.R

**Reactome2Network**
ReactomePathways2UniProtRAT.txt : output from https://github.com/bellsha/Reactome2Network/blob/master/ReactomeClassv2.R

**TOXCASTProc**
*processed datafiles from the 2014 ToxCast release*

ChemAssayBioHitLabels20150703.txt: labels for the toxcast chemicals and assays, used in the NodeEdgeLabel.R, https://github.com/bellsha/cpAOP/blob/master/ToxCastDataprocessing.R

ToxCastChemAssayRatPathNodes20150703.txt: nodes for the toxcast chemicals and assays for reactome, used in the NodeEdgeLabel.R, https://github.com/bellsha/cpAOP/blob/master/ToxCastDataprocessing.R


**Main Directory
*Results files *

cpAOPNetworkFile.cys: Cytoscape file containing the networks presented in this work (cpAOPnetwork, the CCl4 cpAOPsubnet, and the fatty liver cpAOPsubnet), networks generated through: https://github.com/bellsha/cpAOP/blob/master/cpAOPextraction.R

ChemicalsforFLnetwork.txt: List of 37 chemicals that were second neighbors to all 3 of the AOs.

NodeLabels.txt: Annotation for the nodes in the dataset. ID=nodeID, altID=human-readable ID, Group=what data type did it belong to, ClassUpper=higher level grouping, ClassLower=lower level grouping (described in materials and methods) Generated through https://github.com/bellsha/cpAOP/blob/master/NodeEdgeLabel.R

NetworkTable.txt: A tab delimited file containing the edges used to form the cpAOPnetwork. V1/V2=Node ID; V1.name/V2.name= altID; human readable label; SINGLE_REPEAT_TYPE= TG_GATES label referring to first 24hrs (Single) or repeat dosing (Repeat) measure; support/interest= parameters coming from FIM; PadJ= adjust p value for enrichment; UniProtID= the Uniprot ID(s) used to make an association; treatment=treatment combination that yielded the association; DOSE_LEVEL= dose level (low, middle, high) from TG-GATES; SACRIFICE_PERIOD= when the animal was sacrificed, Change=for phenotypic associations, if the effect was increased/decreased relative to normal; ID=association ID. Generated through: https://github.com/bellsha/cpAOP/blob/master/cpAOPextraction.R

*mapping and transitional files needed if not doing full workflow*

TC2TGgatesChemMap20150204.txt- maps the TGGATES chemcials to the ToxCast chemicals https://github.com/bellsha/cpAOP/blob/master/TC2TGGateschemmap.R

LiverPhenotypeLabels.txt: manually curated labels

LiverTCAReactomePhenoChemGraph.txt: Trasitional version of NetworkTable (column labels are the same, just missing the human readable labels). https://github.com/bellsha/cpAOP/blob/master/NodeEdgeLabel.R



