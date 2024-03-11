# Rowan pKa - Supplementary Information

This repository contains the supporting information for [Rowan's recent preprint on pKa prediction](https://chemrxiv.org/engage/chemrxiv/article-details/65ea085be9ebbb4db932e838). 
We hope that this collection of test datasets can be useful for future work in pKa prediction.

## Fitting

The fit dataset was adapted from [Thapa and Raghavachari](https://pubs.acs.org/doi/abs/10.1021/acs.jctc.9b00606), filtering out any SMILES strings that could not be parsed by RDKit. This resulting in 215 molecules and pKa values, which can be found in ``TR215.csv``.

## Evaluation

Eight different datasets used to benchmark Rowan pKa are included in ``assays/``, and the results can be visualized by running ``plot_assay.ipynb``. Here's where the data comes from:

#### SAMPL6 (``assays/SAMPL6.csv``)

Data for SAMPL6 was obtained from [the SAMPL6 Github repository](https://github.com/samplchallenges/SAMPL6/blob/master/physical_properties/pKa/experimental_data/pKa_experimental_values.csv).
We compared the experimentally measured macroscopic pKa values to the microscopic pKa values computed by Rowan, considering only the most acidic and basic microscopic sites on each molecule: we compared each one to the closest macroscopic value, [consistent with the matching procedures detailed here](https://github.com/samplchallenges/SAMPL6/tree/master/physical_properties/pKa/analysis/analysis_of_typeIII_predictions_24mol). This had the effect of excluding doubly ionized microstates.

#### SAMPL7 (``assays/SAMPL7.csv``)

Data for SAMPL7 was obtained from [the SAMPL7 Github repository](https://github.com/samplchallenges/SAMPL7/blob/master/physical_property/pKa/analysis/macrostate_analysis/pKa_experimental_values.csv). Since only one pKa value was obtained for each molecule, assignment was straightforward.

#### Amine Oxetanes (``assays/amine_oxetane.csv``)

Data were obtained from [this paper](https://pubs.acs.org/doi/10.1021/jm9018788).

#### α-CF<sub>3</sub> Bridged Bicyclic Amines (``assays/enamine_aCF3_bicycles.csv``)

Data were obtained from [this paper](https://www.sciencedirect.com/org/science/article/abs/pii/S1434193X23012835).

#### Aromatic *N*-Heterocycles (``assays/ArN.csv``)

Data were obtained from [this paper](https://chemistry-europe.onlinelibrary.wiley.com/doi/abs/10.1002/ejoc.201700749).

#### Folate Inhibitors (``assays/di_kerns_folate.csv``)

Data were obtained from [*Drug-Like Properties: Concepts, Structure Design and Methods from ADME to Toxicity Optimization*](https://www.amazon.com/Drug-Like-Properties-Concepts-Structure-Optimization-dp-0128010762/dp/0128010762), by Li Di and Edward Kerns.

#### BACE1 Inhibitors (``assays/bace.csv``)

Data were obtained from [this paper](https://www.sciencedirect.com/science/article/abs/pii/S0223523421008771?via%3Dihub).

#### Tricyclic Thrombin Inhibitors (``assays/TCT.csv``)

Data were obtained from [this paper](https://chemistry-europe.onlinelibrary.wiley.com/doi/10.1002/cmdc.200700059).

*Corin Wagen, 2024*
