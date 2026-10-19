# CS156---Semester-Project

# How does ADAR1 recoding change residue ionization in squid HOPS/CORVET proteins?

The pipeline trains pKa models on computed pKa values (pKPDB), tests them on measured pKa values (PKAD-2), and applies them to 263 ADAR1-edited residues in 8 *D. pealeii* HOPS/CORVET proteins.

**Main notebook:** `Machine Learning Pipeline 1 - Capstone Part.ipynb`.

## Data
| File (exact name expected) | Source | In this repository? |
|---|---|---|
| `pkas.csv` | pKPDB pKa values, https://pypka.org/pKPDB/ | No, download it |
| `similarity090.csv` | pKPDB similarity clusters, same page | No, download it |
| `PKAD2_wild_2026-10-17T20_4411.527Z.csv` | PKAD-2, https://compbio.clemson.edu/pkad-2/ (rename your download to this) | No, download it |
| `D pealeii ORFs (1).fa`, `Editing Sites (1).xlsx` | Rosenthal Lab (MBL) | Yes, in `DP FILES - PIPELINE - With other files.zip` |
| `edited_residues_DP.csv` | output of Step 1 | Yes, in the 'DP FILES - PIPELINE - With other files.zip' |

The RCSB 30% sequence clusters and the PDB structures are downloaded automatically.

## How to run
1. `pip install -r requirements.txt`
2. Please download and put all the data files in one folder, and set `PIPELINE_DATA` to that folder (or edit the `DATA` code lines in the first code cell).
3. Run all cells.


## AI use
I used Claude in the summer to replace the manual mapping of editing sites onto the ORF, and then translating it. I incorporated that in my assignment. Besides that I used Claude to help me with the coding and resolve any coding errors. I designed the majority of the pipeline and the analysis sections by myself. I also used Claude to critique my analysis and help me improve the depth of this pipeline. I did not use it to generate text from scratch for this assignment. 
