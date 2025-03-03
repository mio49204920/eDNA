# Workflow for Environmental DNA Analysis Using Mitochondrial Universal 16S rRNA Primers

In environmental DNA (eDNA) analysis, studies typically focus on specific taxonomic groups such as fish, birds, and mammals. However, a primer that enables the comprehensive detection of biological species in a single sequencing run has not yet been established. Furthermore, conventional eDNA analysis mainly relies on short-read sequencing using the Illumina MiSeq, one of the next-generation sequencers, which has a limitation on read length. By amplifying the 16S gene region using the 16S ar and br primers, which have been traditionally used for species identification with Sanger sequencing, and analyzing it with Oxford Nanopore, a next-generation sequencer capable of long-read sequencing, it is possible to achieve a more comprehensive species detection method.

## How to use

Ensure that seqkit, blastn, blast2rma, and rma2info are included in the system's PATH to allow seamless execution from any directory.

```
wget https://github.com/mio49204920/eDNA/releases/download/0.1/merged_12.2_1.15.fa.tar.gz
tar vxf merged_12.2_1.15.fa.tar.gz
makeblastdb -in merged_12.2_1.15.fa.tar.gz -dbtype nucl

git clone https://github.com/mio49204920/eDNA.git
bash ./eDNA/blast/shblast -t 16 <input_fastq>
```
