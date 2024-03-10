# Translation Error Analysis in Drosophila

## Introduction
The purpose of this script is to detect translation error events and identify the characters of error events. Please refer to our article for specific experimental design and description.

## Steps

### Step 1. Detect translation error events from MaxQuant output
The mass spectrometry data were initially subjected to identification of corresponding Base peptides and Dependent peptides using the MaxQuant software. Additionally, a previously published pipeline (Mordret et al., 2019, Mol. Cell) was employed to identify amino acid translation error events and calculate the overall translation error frequency at the codon level. For a detailed description of the process, refer to **TranslationError_01_ErrorDetected.ipynb**.

### Step 2. Inference and statistical analysis of mismatched base pairs in translation errors
For the identified translation error events, an analysis was conducted to statistically assess the potential mismatched base pair positions. The specific computational procedure is outlined in **TranslationError_02_ErrorCharacters.ipynb**.

### Step 3. Simulation of translation error detection
For codons where translation errors were not detected, it was assumed that this was due to underrepresentation resulting from low usage frequency. To account for this, we employed a specified translation error rate and varied the detection depth of mass spectrometry to simulate this process. For a detailed implementation, refer to **TranslationError_03_DetectedSimulation.ipynb**.

### Step 4. Association between Codon Usage Frequency and Translation Error Rate
We investigated the association between codon usage frequency and translation error rate using three different approaches. For a detailed implementation, refer to **TranslationError_04_ErrorRateAndUsage.ipynb** and the corresponding description in the manuscript.

### Step 5. Association between codon usage frequency and ribosomal elongation rate
We analyzed the correlation between the usage frequency of different codons and the codon-level ribosomal elongation rates. For a detailed analytical process, refer to **TranslationError_05_RibosomeElongation.ipynb** and the corresponding description in the manuscript.

### Step 6. Selection on Mutations Causing Changes in Codon Usage Frequency in Drosophila
We compared the frequency distribution of mutations causing changes in codon usage frequency in a population of Drosophila melanogaster. Additionally, the MK test was employed to calculate the proportion of mutations subjected to positive selection. For the analysis process, refer to **TranslationError_06_NatureSelection.ipynb** and the corresponding description in the manuscript.

## License
Each file included in this repository is licensed under the MIT License.
