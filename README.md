# Genomic Data Science

First-time bioinformatics work in Python using Biopython, covering sequence parsing, BLAST searches against NCBI databases, and a handwritten module containing functions whose input is a FASTA file leading to outputs such as record counting, sequence length stats, and open reading frame detection.

These are basic things meant for practising coding in a computational biology/bioinformatics setting, PEP 8 style, and Google style docstrings to familiarise myself with what best practice is.

## What's in here

- **`BiopythonFirstExposure.ipynb`**: A self-introduction to the `Biopython` library.
    - Running BLAST searches `Bio.Blast.NCBIWWW` against NCBI's nucleotide database 
    - Running BLAST alignment to identify the most likely origin of unknown DNA sequence
    - Working with `Seq` object by going through its documentation and using `complement()`, `reverse_complement()`, `translate()`, etc.

- **`SeqDataAnalysis.ipynb`**: A basic sequence data analysis toolkit written from scratch without `Biopython` based on input from a Multi-FASTA file.
    - Extracts from Multi-FASTA files and stores sequences in a dictionary format
    - Reports basic numbers such as record counting, lengths of sequences, longest and shortest sequences with their sequence identifiers, etc.
    - (Work in progress) Detects all open reading frames (ORFs) given a certain reading frame and finds longest ORFs per sequence per Multi-FASTA file
    - (Work in progress) Detects all repeats of a given length and finds the most frequent repeat of a given length

- **`dna.example.fasta`**: A sample Multi-FASTA file for the purpose of running **`SeqDataAnalysis.ipynb`**.

## Tools and Libraries

- Python 3.13
- Biopython
- Jupyter Notebook

## Key Takeaways

- Built from scratch an ORF-finding algorithm for any given reading frame without relying on external bioinformatics tools
- Used BLAST via `Biopython` to identify the origin organism of a DNA sequence
- Practised translating between manual sequence parsing and through the `Seq` object in `Biopython`

## How to run

1. Clone this repo:
```
git clone https://github.com/SourMangoMan/genomic-data-science.git
```

2. Install the packages:
```
pip install Biopython
```
3. Open notebooks in Jupyter or VS Code and run from top to bottom. **`SeqDataAnalysis.ipynb`** uses **`dna.example.fasta`** as its data input.
