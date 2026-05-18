# ABI Summer School 2026: Introduction to Linux Basics

### Module 1: Linux & HPC | Day 1 

---

## Overview

This repository contains the materials for the **Introduction to Linux Basics** - a hands-on 
exercise for the ABI Summer School 2026. Participants download a realistic
bioinformatics project directory and work through it using Linux commands.

The scenario: you are a research assistant on a multi-country *Plasmodium falciparum*
genomics study. The lead researcher has had to leave unexpectedly. The supervisor meeting
is at 9am Monday. The project folder is on the cluster. Your job is to find your way
around it, organise what was left behind, and make sure everything is in order.

---

## What is in this repository

```
abi-summer-school-project/
├── ABI_summer_school_project.zip          ← The project directory (participants download this)
└── README.md                              ← This file
```

---

## For Participants — Getting Started

Log into the cluster, then run:

```bash
wget https://github.com/[YOUR_GITHUB_USERNAME]/abi-linux-scavenger/raw/main/ABI_summer_school_project.zip
```

Unzip it:

```bash
unzip ABI_summer_school_project.zip
```

Go inside:

```bash
cd ABI_summer_school_project
```

Read the opening note:

```bash
cat README.txt
```

---

## What this session Covers

The exercise is divided into **three levels**, each building on the last.

| Level | Theme | Commands |
|-------|-------|----------|
| 🟢 Level 1 | Get In and Look Around | `wget` · `unzip` · `pwd` · `ls` and all options · `cd` · absolute and relative paths · `cd -` |
| 🟡 Level 2 | Handle the Data | `cat` · `head` · `tail` · `less` · wildcards · hidden files · `mkdir` · `touch` · `nano` · `cp` · `ln -s` · `mv` · `rm` |
| 🔴 Level 3 | Search and Discover | `sort` · `comm` · `join` · `find` · `wc` · `grep` · `cut` · `paste` |

---

## What is inside `ABI_summer_school_project.zip`

A realistic bioinformatics project directory with clean biological data files.

```
ABI_summer_school_project/
├── README.txt
├── raw_data/
│   ├── sample_manifest.tsv          ← 10 Plasmodium falciparum samples, 3 field sites
│   ├── coverage_report.tsv          ← Sequencing coverage per sample
│   ├── batch1_samples.txt           ← Sample list for comm/sort exercises
│   ├── batch2_samples.txt           ← Sample list for comm/sort exercises
│   ├── SAMPLE_001.fastq             ← Raw sequencing reads
│   ├── SAMPLE_002.fastq ... (10 total)
│   └── .hidden_note.txt             ← Hidden file (found with ls -a)
├── reference/
│   ├── Pfalciparum_3D7.fasta        ← Reference genome (FASTA format)
│   └── Pfalciparum_3D7.gtf          ← Gene annotation (GTF format)
├── variants/
│   ├── SAMPLE_001.vcf               ← Variant calls (VCF format)
│   └── SAMPLE_002.vcf
├── logs/
│   └── pipeline.log                 ← Pipeline run log with INFO/WARNING/ERROR lines
├── scripts/
│   └── run_pipeline.sh              ← Incomplete pipeline script
├── results/                         ← Empty — participants build the structure
└── .backup/
    └── original_sample_ids.txt      ← Hidden directory (found with ls -a)
```

**File formats encountered:**

| Format | Description |
|--------|-------------|
| `.fastq` | Raw sequencing reads — 4 lines per read |
| `.fasta` | Reference genome sequences |
| `.vcf` | Variant Call Format — SNPs and INDELs |
| `.gtf` | Gene annotation coordinates |
| `.tsv` | Tab-separated values — sample metadata |
| `.log` | Pipeline run logs |

---

## Learning Outcomes

By the end of the scavenger hunt, participants will have practised:

- Downloading files from the web with `wget` and extracting with `unzip`
- Navigating a realistic project directory structure
- Reading biological file formats from the command line
- Managing files — creating, copying, moving, renaming, deleting
- Creating symbolic links
- Finding and reading hidden files
- Sorting files and comparing sorted lists with `comm`
- Joining two files on a common field with `join`
- Searching file contents with `grep` and `find`
- Extracting and counting data with `wc`, `cut`, and `paste`
- Using wildcards to work with multiple files at once

---

## Next Session

After this exercise, the next session covers **pipes, filters, and brace expansion**.
Many commands used individually in this hunt — `grep`, `cut`, `wc`, `find`, `sort`, `uniq`
— will be chained together using `|` to build more powerful one-liners.
This exercise is deliberately designed so that the pipes session feels like a natural upgrade.

---

*ABI Summer School 2026 · African Bioinformatics Initiative*
