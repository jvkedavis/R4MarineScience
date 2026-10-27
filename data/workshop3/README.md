# Data for: Kelp forest loss and emergence of turf algae reshapes energy flow to predators in a rapidly warming ecosystem

Dataset DOI: [10.5061/dryad.bcc2fqzqz](10.5061/dryad.bcc2fqzqz)

## Description of the data and file structure

Our study took place in four subregions of the Maine coast that span a gradient of temperature and kelp forest habitat condition. At each study site, we conducted surveys to quantify available basal resources (macroalgae) and characterize the fish assemblage. We then collected representative primary producers and the two dominant fish species for stable isotope analysis. We analyzed these fish using both bulk tissue and compound-specific stable isotope analyses to document fish isotopic niches and energy use on kelp-dominated vs. red turf algae-dominated  reefs.

## Files and variables

### File: Data1\_macroalgae\_biomass.csv

**Description:** This dataset contains measurements of seaweed biomass (i.e., kelp, red macroalgae, and other seaweeds) collected from replicate 1 square meter quadrats (n = 4-6 per site) at multiple sites and subregions in coastal Maine. Macroalgae biomass surveys were conducted during the summers of 2021 and 2022 on shallow, subtidal rocky reefs (5-7 m depth MLLW) across Maine’s exposed outer coast.

* See “Section 1: Underwater surveys” in the methods for details.

##### Variables

* **survey_date**: the date on which the survey was conducted
* **site**: the name of the location where the survey took place, corresponds to **lat** and **long**
* **region**: the subregion of coastal Maine encompassing the study **site** (*Casco Bay*, *Midcoast*, *Penobscot* *Bay*, or *Downeast*)
* **lat**: latitude coordinate of survey **site** (*decimal degrees* of transect, meter mark 0)
* **long**: longitude coordinate of survey **site** (*decimal degrees* of transect, meter mark 0)
* **meter_mark**: the distance (in *meters*) along a given transect where the quadrat was placed for sample collection
* **taxa**: the lowest taxonomic classification to which the sample was identified in the lab. This is either a species, a genus, or a morphological grouping. Note: in 2021, *Vertebrata* species were identified to species level (*V. fucoides* or *V. nigra*) when possible, whereas in 2022, they were always combined as *Vertebrata* spp.
* **group**: a broader classification based on higher-level taxonomy and morphology (*kelp, brown_other, green,  red_turf,  red_other*)
* **mass_g**: the mass (biomass) of the sampled macroalgae, scaled to *grams per square meter*. Samples were spun (in a salad spinner or mesh bag) to remove excess water before weighing. ‘NA’ = biomass measurement is missing

### File: Data2\_roving\_fishes.csv

**Description:** This dataset contains fish count and length (in 2.5 cm size bins) estimates recorded during surveys of replicate 40 x 2 m transects on subtidal rocky reefs across the coast of Maine. Biomass (in grams) of each individual was computed using a known, species-specific length-weight relationship.

We used 2.5 cm “size bins” to estimate fish total length. The smallest size bin was 1-2.5 cm, and then bins increased in increments of 2.5 cm (2.5-5, 5-7.5, 7.5-10, etc.). However, some estimates are integrated across multiple bins; for example, when sizing fish from a distance, or schools with many individuals of differing sizes.

Note: each row is an observation, and in many cases, multiple observations were made per transect. ‘na’ = not applicable.

* See “Section 1: Underwater surveys” in the methods for more details.

##### Variables

* **survey_date**: the date when the fish  survey was conducted
* **region**: the subregion of Maine encompassing the study **site** (*Casco Bay*, *Midcoast*, *Penobscot Bay*, or *Downeast*)
* **site**: the name of the location where the survey took place, corresponds to **lat** and **long**
* **lat**: latitude coordinate of survey **site** (*decimal degrees* of transect 1, meter mark 0)
* **long**: longitude coordinate of survey **site** (*decimal degrees* of transect 1, meter mark 0)
* **visibility_m**: water visibility at the site in *meters*, measured by divers as the maximum horizontal distance from which they could see a Secchi disk. A single measurement was taken per survey. ‘NR’ indicates that visibility was not recorded during the survey
* **transect**: identifier for the transect replicate along which fish were observed and measured (1, 2, or 3). Transects were 40 m x 2 m and ran parallel to the reef at ~5-7 m depth. There was a minimum of 10 m between transects
* **taxa**: the identity (common name) of the fish observed. ‘no_fish’ indicates no fish were observed along the transect. Fish taxa include *pollock* (*Pollachius virens*), *cunner* (*Tautogolabrus adspersus*), *gunnel* (*Pholis gunnellus*), *cod* (*Gadus morhua*), sculpin (*Myoxocephalus* spp.), and winter_flounder (*Pseudopleuronectes americanus*)
* **length_min**: the minimum end of the size bin for the observed fish, in *centimeters*
* **length_max**: the upper end of the size bin for the observed fish, in *centimeters*
* **length_cm**: length estimate in *centimeters*, based on average of **length_min** and **length_max**
* **count**: counted or estimated number of fish in a given observation
* **a**: species-specific coefficient ‘a’ for calculating biomass from length, derived from length-weight parameters on [FishBase](https://www.fishbase.se/search.php)
* **b**: species-specific coefficient ‘b’ for calculating biomass from length, derived from length-weight parameters on [FishBase](https://www.fishbase.se/search.php)
* **biomass_g**: the estimated biomass of fish (single or multiple individuals) in a given observation in *grams*, calculated from: (***a*** × **length_cm**^**b** ) ×  **count**![](file:////Users/dara/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image002.png)

### File: Data3\_bulk\_CN\_stable\_isotopes.csv

**Description:** This dataset contains bulk tissue δ¹³C and δ¹⁵N values for primary producers, invertebrates, and fish collected across the coast of Maine in 2022.

* See “Section 2: Isotope sample collection & processing” in the methods for details about sample collection.
* See “Section 3:  Bulk tissue δ¹³C and δ¹⁵N analysis” in the methods for details about sample analysis.

##### Variables

* **sample_code**: unique identifier for each sample. The first letter of the code denotes sample type (‘P’ = particulate organic matter (POM), ‘A’ = macroalgae, “I” = invertebrate whole bodies or tissues, ‘F’ = fish muscle tissue)
* **taxa**: the identity of the sample to the lowest taxonomic level (species, genus, higher taxonomic grouping, or POM)
* **group**: broader taxonomic or functional group, based on **taxa**
* **type**: broader groupings to categorize the sample (*POM*, *macroalgae*, *invertebrate*, or *fish*)
* **region**: the subregion of Maine encompassing the sample collection **site** (*Casco Bay*, *Midcoast*, *Penobscot Bay*, or *Downeast*)
* **site**: the name of the sample collection location
* **lat**: latitude coordinate of the sample collection location (in *decimal degrees*). Some POM collection sites are approximate; these are noted in **notes**
* **long**: longitude coordinate of the sample collection location (in *decimal degrees*). Some POM collection sites are approximate; these are noted in **notes**
* **collection_date**: the date the sample was collected
* **length_mm**: length of the sampled organism in *millimeters*, if applicable. ‘na’ if not measured
* **wet_weight_g**: the measured weight of the sampled organism in *grams.* ‘na’ if not measured. 'nr' = weight measurement is missing
* **d13C**: the stable carbon isotope ratio (δ¹³C) of the sample, measured by IRMS and corrected based on internal standards. Units are per mil (‰)
* **d15N**: the stable nitrogen isotope ratio (δ¹⁵N) of the sample, measured by IRMS and corrected based on internal standards. Units are per mil (‰)
* **C.N**: the carbon-to-nitrogen ratio of the sample, measured by IRMS
* **notes**: additional observations or metadata related to the sample. ‘na’ if no notes were made

### File: Data4\_AA\_d13C\_values.csv

**Description:** This dataset contains stable carbon isotope (δ¹³C) values of individual amino acids for primary producers and predatory fishes following sample hydrolysis, derivatization, and analysis in a gas-chromatography combustion unit coupled to an isotope-ratio mass spectrometer (GC-C-IRMS). The values have been corrected based on internal reference materials. Data about each sample, reference material, and GC-C-IRMS run are included. The corresponding bulk tissue δ¹³C and δ¹⁵N values for these samples are in *Data3_bulk_CN_stable_isotopes.csv*; however, this data file includes  seven additional samples that were collected in 2023. 

Columns with a three-letter amino acid code contain δ¹³C values obtained by GC-C-IRMS, then corrected based on their reference material, or their standard deviation between injections for that amino acid (denoted by ‘SD’). The three-letter code specifies the amino acid (see below). δ¹³C values may be ‘na’ if we did not obtain data for the particular amino acid in that sample. SD values may be ‘na’ if no usable δ¹³C values were collected or only one injection produced usable δ¹³C values. Units are per mil (‰).

* See “Section 2: Isotope sample collection & processing” in the methods for details about sample collection.
* See “Section 4: Stable carbon isotope analysis of essential amino acids (*δ*¹³C<sub>EAA</sub>)” in the methods for details about sample analysis.
* See “Section 5: Flexible discriminant analysis (FDA) to quantify consumer energy channel use” for details on how we use these data to quantify the proportional contribution of various energy channels to consumers.

##### Variables

* **sample_code**: unique identifier for each sample. First letter of code denotes sample type (‘*P*’= particulate organic matter (POM), ‘*A*’ = macroalgae, ‘*F*’ = fish muscle tissue)
* **taxa**: the identity of the sample to the lowest taxonomic level (species, genus, higher taxonomic grouping, or POM)
* **group**: broader taxonomic or functional group, based on **taxa**
* **type**: broader groupings to categorize the sample (POM, macroalgae, or fish)
* **site**: the name of the sample collection location
* **region**: the subregion of Maine encompassing the sample collection **site** (*Casco Bay*, *Midcoast*, *Penobscot* *Bay*, or *Downeast*)
* **collection_date**: the date the sample was collected
* **length_mm**: length of the sample organism in *millimeters*, if applicable. ‘na’ if not measured
* **hydrolysis_mass_mg**: mass of the sample used for hydrolysis in *milligrams*. ‘na’ if not applicable, as for POM samples, since the samples were on a filter
* **ref_1**: identifier for one internal reference material with which the sample was   derivatized. The three-letter code denotes standard type (UNM or STD), the second three-number code denotes standard batch
* **ref_2**: identifier for a second internal reference material with which the sample was   derivatized. The three-letter code denotes standard type (UNM or STD), the second three-number code denotes standard batch. ‘na’ if only one internal reference material was made with the respective hydrolysis batch
* **runID**: numeric identifier for the GC-C-IRMS run
* **run_date**: date of the GC-C-IRMS run
* **STD**: identifier number of the reference material which was run on the GC-C-IRMS alongside the sample in question and used to correct the δ¹³C values for each amino acid (3-number code corresponding to **ref_1** or **ref_2**)
* **STD.t**: type of the reference material which was run on the GC-C-IRMS alongside the sample in question and used to correct the δ¹³C values for each amino acid (*UNM* or *STD*, corresponding to number code in **ref_1** or **ref_2**)
* **N.inj**: number of injections made for the sample during analysis, from which the following values were derived
* **Ala13C**: alanine δ¹³C value, ‰
* **Ala13C.SD**: alanine δ¹³C standard deviation between injections
* **Gly13C**: glycine δ¹³C value, ‰
* **Gly13C.SD**: glycine δ¹³C standard deviation between injections
* **Thr13C**: threonine δ¹³C value, ‰. This is an essential amino acid
* **Thr13C.SD**: threonine δ¹³C standard deviation between injections
* **Ser13C**: serine δ¹³C value, ‰
* **Ser13C.SD**: serine δ¹³C standard deviation between injections
* **Val13C**: valine δ¹³C value, ‰. This is an essential amino acid
* **Val13C.SD**: valine δ¹³C standard deviation between injections
* **Leu13C**: leucine δ¹³C value, ‰. This is an essential amino acid
* **Leu13C.SD**: leucine δ¹³C standard deviation between injections
* **Ile13C**: isoleucine δ¹³C value, ‰. This is an essential amino acid
* **Ile13C.SD**: isoleucine δ¹³C standard deviation between injections
* **Pro13C**: proline δ¹³C value, ‰
* **Pro13C.SD**: proline δ¹³C standard deviation between injections
* **Asp13C**: aspartic acid δ¹³C value, ‰
* **Asp13C.SD**: aspartic acid δ¹³C standard deviation between injections
* **Glu13C**: glutamic acid δ¹³C value, ‰
* **Glu13C.SD**: glutamic acid δ¹³C standard deviation between injections
* **Phe13C**: phenylalanine δ¹³C value, ‰. This is an essential amino acid
* **Phe13C.SD**: phenylalanine δ¹³C standard deviation between injections
* **Tyr13C**: tyrosine δ¹³C value, ‰
* **Tyr13C.SD**: tyrosine δ¹³C standard deviation between injections
* **Lys13C**: lysine δ¹³C value, ‰. This is an essential amino acid
* **Lys13C.SD**: lysine δ¹³C standard deviation between injections
* **Arg13C**: arginine δ¹³C value, ‰
* **Arg13C.SD**: arginine δ¹³C standard deviation between injections

### File: Data5\_FDA\_consumer\_means.csv

**Description:** This dataset is the output from a bootstrap resampling of a flexible discriminant analysis (FDA) classification of consumer (predatory fish) energy channels. This dataset can be directly derived from δ¹³C data of five essential amino acids (Ile, Leu, Thr, Val, and Phe) from *Data4_AA_d13C_values.csv*; however, because resampling randomly subsets the primary producer data, there may be slight deviations in each iteration. This output was used in our analyses and figure generation.   

* See “Section 4: Stable carbon isotope analysis of essential amino acids (*δ*¹³C<sub>EAA</sub>)” in the methods for how the original *δ*¹³C<sub>EAA</sub> measurements were made.
* See “Section 5: Flexible discriminant analysis (FDA) to quantify consumer energy channel use” for details on how this dataset was derived.

##### Variables

* **sample_code**: unique identifier for the sample. All samples are predatory fish (pollock or cunner), and their sample metadata (including which subregion they are from) and original EAA δ¹³C values can be found in *Data4_AA_d13C_values.csv*
* **K.mean**: mean probability (from **N** bootstrap iterations) that the EAA of this fish was derived from *kelp*
* **K.sd**: standard deviation of *kelp* estimates
* **P.mean**: mean probability (from **N** bootstrap iterations) that the EAA of this fish was derived from *phytoplankton*
* **P.sd**: standard deviation of *phytoplankton* estimates
* **R.mean**: mean probability (from **N** bootstrap iterations) that the EAA of this fish was derived from *red macroalgae*
* **R.sd**: standard deviation of *red macroalgae* estimates
* **N**: number of iterations used to calculate the means and standard deviations. Set to 10,000

### File: Data6\_POM\_18S.csv

**Description:** This dataset is derived from amplicon sequencing of the 18SV4 gene region, and taxonomic assignments were made using a *dada2* bioinformatics pipeline with the PR2 database. We retained all ASVs that were among the 99% most abundant in each sample, and grouped them here based on species-level taxonomic assignments.

* See “Section 2: Isotope sample collection & processing” in the methods for details about POM sample collection.
* See “Section 6: Particulate organic matter (POM) as a proxy for phytoplankton” in the methods for details about POM sample sequencing and data processing.

##### Variables

* **sample_code**: unique identifier for the POM sample, which matches those in the bulk (*Data3_bulk_CN_stable_isotopes.csv*) and amino acid (*Data4_AA_d13C_values.csv*) stable isotope datasets
* **region**: subregion of Maine where the POM sample was collected. Samples were collected at a depth of ~1m below the surface and ~ 1km offshore of the nearest coastline
* **tax.Kingdom**: kingdom-level taxonomic classification, from a *dada2* assignment based on the PR2 database
* **tax.Supergroup**: supergroup-level taxonomic classification, from a *dada2* assignment based on the PR2 database
* **tax.Division**: division-level taxonomic classification, from a *dada2* assignment based on the PR2 database
* **tax.Class**: class-level taxonomic classification, from a *dada2* assignment based on the PR2 database
* **tax.Order**: order-level taxonomic classification, from a *dada2* assignment based on the PR2 database
* **tax.Family**: family-level taxonomic classification, from a *dada2* assignment based on the PR2 database
* **tax.Genus**: genus-level taxonomic classification, from a *dada2* assignment based on the PR2 database
* **tax.Species**: species- or lowest taxonomic-level classification, from a *dada2* assignment based on the PR2 database
* **group**: manually assigned ecological or functional grouping based on *dada2* taxonomic assignments
* **phytoplankton**: categorical indicator of whether the taxon is phytoplankton. ‘*yes’* if the group is an autotrophic microalgae. ‘*no’* if other (e.g., microheterotrophs or animals)
* **read_abundance**: total number of sequence reads for the taxon in the sample
* **read_proportion**: proportion of reads for the taxon relative to the total reads in the sample