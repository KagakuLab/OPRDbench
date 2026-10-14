OPRDbench: A Manufacturing Chemistry Benchmark for CASP Tools
=============================================================

This repository contains a benchmark dataset of target molecules extracted from the
**Organic Process Research & Development** (OPRD) journal, intended for the evaluation
of Computer-Aided Synthesis Planning (CASP) tools on manufacturing chemistry targets.

Motivation
----------

Modern computer-aided synthesis planning (CASP) tools have demonstrated their usefulness
for the ideation stage of chemical synthesis route design. However, the same target
molecule can be synthesized via substantially different routes depending on the purpose:
a discovery route used to obtain small quantities during early development, or a
manufacturing route optimized for industrial-scale production. While CASP tools have
been extensively benchmarked on discovery chemistry targets, their potential to support
manufacturing route design remains largely unexplored, and public benchmark datasets
focused on process chemistry are lacking.

This benchmark takes a first step in this direction by collecting target molecules from
OPRD - one of the main sources of process chemistry research - and pairing each target
with the DOI of its source publication, so that the corresponding expert-designed
manufacturing route can be retrieved directly from the literature and compared with
CASP predictions.

Dataset
-------

The dataset `OPRDbench_1997_2022.csv <https://github.com/KagakuLab/OPRDbench/blob/main/OPRDbench_1997_2022.csv>`_ contains **2219 unique target molecules** extracted
from OPRD publications covering the period 1997-2022.

Each entry consists of:

- **target** - the target molecule in SMILES format
- **doi** - the DOI of the source OPRD publication

.. note::
   The dataset contains only target structures and literature references.
   Synthetic routes are **not** digitized and can be retrieved from the cited publications.

The relationship between entries is not strictly one-to-one: the same molecule may appear
in multiple papers reporting different routes (one SMILES → several DOIs), and a single
paper may report routes to several targets (one DOI → several SMILES entries).

Usage
-----

- Use the target molecules in your CASP to evaluate how many targets your method can solve
- For the solved targets, compare your predicted routes with the expert-designed routes reported in the original paper

Preprint
-----

More details can be found in preprint: https://chemrxiv.org/doi/full/10.26434/chemrxiv.15010421/v1
