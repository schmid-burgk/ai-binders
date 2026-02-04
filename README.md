# Transposon-Display

This repository contains the analysis files used to generate the figures presented in [*Transposon-Display of AI-designed binders enables manipulation of the proteome in human cells*](https://www.biorxiv.org/content/10.1101/2025.05.11.653342v1).

All tools are also available and *directly executable* via our [website](www.jsb-lab.bio/ai-binders).  
X/Y plots were generated using the [xyplot tool](https://jsb-lab.bio/xyplot/).

---

## Short Description

Transposon-Display is a wet-lab pipeline for the rapid identification and optimization of binders from large candidate libraries.

---


## 1. System requirements

### Operating Systems
- Tested on:
  - Ubuntu 22.04
  - macOS 13+
  - Windows 10/11

### Software Dependencies
- Python 3.10

The software has been tested with Python 3.10 on the operating systems listed above.


A complete list of dependencies is provided [*here*](./requirements.txt).

### Hardware Requirements

The software does not require specialized hardware. All analysis files can be run on a standard desktop or laptop computer.

### Installation Time

Typical installation time is approximately 5 minutes on a standard desktop or laptop computer.

---

## 2. Provided Tools

### [**AI Binder Counter**](AnalyzeTpDisplay_v1.htm)

Binder abundances before and after pulldown were quantified directly from raw sequencing data. This tool counts individual AI binder sequences to assess enrichment across experimental conditions.

Example data for a Transposon-Display experiment is provided.  
Further instructions and a demo are available [*here*](./TP-Display_analyzer.md).

---

### [**Saturation Mutagenesis Pool Design**](DesignSaturationMutagenesisPools_v1.htm)

These tools were used to generate saturation mutagenesis pools for the AI-designed binders and the transposase described in the preprint. The resulting oligonucleotide pools contain a triplet of degenerate bases for every amino acid position in the input sequence (Figure 1).

Sequences are tiled into fragments of approximately 118 bp and include 3–5 silent mutations flanking each targeted residue. These silent mutations enable robust discrimination between sequencing errors and intentionally introduced degenerate codons.

Example data for transposase pool generation is provided.  
Further instructions and a demo are available [*here*](./saturation_mutagenesis_design.md).

---

### [**Saturation Mutagenesis Evaluation**](AnalyzeSaturationMutagenesis_v1.htm)

Sequencing data from saturation mutagenesis pools are analyzed by identifying the mutated amino acid via the surrounding silent mutations and quantifying their occurrences in the sequencing data. The wild-type sequence is also quantified as a quality control. Stop codons are denoted as `x`.

Example data for the evaluation of a Transposon-Display saturation mutagenesis experiment is provided.  
Further instructions and a demo are available [*here*](./saturation_mutagenesis_evaluation.md).

---

## Getting Started

1. Install [Miniconda](https://conda.io/miniconda.html)

2. Clone this repository:  
   Open a terminal and run:
   ```bash
   git clone https://github.com/schmid-burgk/TP-Display.git
   cd TP-Display
   ```

3. Activate conda and install required packages:
    ```bash
    conda activate
    pip install -r requirements.txt
    ``` 
4. Open the notebooks
    ```bash
    jupyter lab
    ``` 

5. Javascript htm files can be downloaded and run in any modern browser. 

