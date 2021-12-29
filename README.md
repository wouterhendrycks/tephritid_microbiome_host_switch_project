# tephritid_microbiome_host_switch_project
Contains the scripts and data tables used in the analysis of microbiome data from a project on changes in the microbiome of the tephritid Z. cucurbitae when feeding on non-cucurbit host plants compared to cucurbit host plants. Raw sequence data has been deposited at the European Nucleotide archive. 

The script outlines the DADA2 pipeline (Callahan et al., 2016) that was used to process raw sequence reads, the decontam pipeline used to remove potential contaminants and the subsequent statistical analyses that have been conducted on the processed data. The subsequent analysis includes: 
         1. the identification of core microbial taxa using the AU-test of Hester et al. (2016).
         2. the univariate analysis of diversity metrics (ACE, Inverse Simpson and Faith's PD) through linear mixed models. 
         3. the computation of Generalized and Unweighted Unifrac distances on the dataset with singleton taxa filtered (as suggested by Chakrabarti et al., 2016, Clarke et al., 2019) and were the abundance of bacteria was converted into proportions (McKnight et al., 2019). These distances were subsequently used for multivariate analysis with PERMANOVA analysis using PRIMER7. 
         4. The identification of differentially abundant taxa using ALDEx2 (Fernandes et al., 2013).
         5. The identification of predicted metabolic pathways using Tax4Fun2 (Wehmheuer et al., 2020).
         6. The making of various accompanying boxplots, barplots and heatmaps.

The Tab_Unifrac_test2 file contains the frequency table of all taxa found in the samples with their relative abundance for each sample and with singleton taxa removed. This datafile has been used for the computation of the Unifrac distances and the subsequent multivariate analysis.

The frequency table excel sheet contains the frequency table of all taxa found in the samples with their absolute abundance for each sample and with the taxonomic classification of each taxon found in the data. This dataset is the outcome that is obtained after the DADA2 pipeline and the removal of potential contaminants through decontam.

The metadata file contains the corresponding metadata of this project.
