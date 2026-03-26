---
title: '...'
title_short: 'SWAT4HCLS26 #8: flatviewfs'
tags:
  - virtual file system
  - tabular database
  - variant call format (VCF) data
authors:
  - name: Elias Crum
    orcid: 0009-0005-3991-754X
    affiliation: [1,2]
    role: VCF to TSV conversion, duckDB data ingestion, manuscript writing + editing
  - name: Benno Kruit
    orcid: 0000-0002-0228-4823
    affiliation: 3
    role: FUSE virtual file generation from duckDB data, manuscript writing + editing
affiliations:
  - name: IDLab, Department of Electronics and Information Systems, Ghent University – imec, Belgium
    index: 1
  - name: Flemish institute for Technological Research (VITO) Mol, Belgium
    index: 2
  - name: example
    index: 3
date: 26 March 2026
cito-bibliography: paper.bib
event: SWAT4HCLS26 
biohackathon_name: "BioHackathon SWAT4HCLS 2026"
biohackathon_url:   "https://biohackathon-europe.org/"
biohackathon_location: "Amsterdam, The Netherlands, 2026"
group: Project 8
# URL to project git repo --- should contain the actual paper.md:
git_url: https://github.com/ecrum19/flatviewfs_report
# This is the short authors description that is used at the
# bottom of the generated paper (typically the first two authors):
authors_short: Elias Crum and Benno Kruit
---


# Introduction

This report describes the design and implementation of a tool that serves a virtual flat-file view over data stored in a relational representation. The central idea is to preserve the queryability and compact storage of a tabular backend while exposing the data through a conventional file interface that can be inspected with standard filesystem operations. In this work, compressed storage is provided through Apache Parquet, a columnar format designed for efficient storage and retrieval with built-in compression and encoding support, while DuckDB is used as the embedded analytical database managing the relational view of the data. The file-oriented presentation layer is implemented with FUSE, which enables user-space programs to export filesystems to the kernel and thereby present generated content as ordinary files. 

As a concrete demonstration, the tool is applied to genomic variant data represented in Variant Call Format (VCF). VCF is a text-based format consisting of meta-information lines, a header, and tab-delimited variant records with genotype information for one or more samples, making it a natural target for virtual flat-file materialization from relational tables. This setting provides a useful test case because VCF combines structured schema-like fields with a strict textual serialization, allowing the system to illustrate how relational records can be reconstructed into a standards-compliant, human-readable file without duplicating the underlying dataset. 


# Results


# Discussion

...

## Acknowledgements

...

## References
