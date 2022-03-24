# SKiM

A backend PubMed text index is required for executing SKiM. The code for building the backend PubMed text index is available at https://github.com/iross/km_indexer. In SKiM_chtc_query2.py, the user should assign their backend PubMed text index for the variable URL_BASE in line 13. The user should change the username and password in line 14, if applicable.  

Basic syntax for executing SKiM:   
$ python production_SKiM.py keyphrase level_1_file level_2_file output_dir num_level2_queries  
   
Authors: Kalpana Raja and John Steill  
   
Affiliation: Morgridge Institute for Research, Madison, WI, USA.   

# Instructions
start docker containers with Elastic DB and PostGres DB if base is already made or run docker compose for km_indexer.

## Project commands
python production_SKiM.py data/rheumatoidArthritis_genes.txt data/B_terms_file_rheumatoid_arthritis.txt data/rheumatoidArthritis_drugs_TTDandDgidb.txt rhArthritis_2005/ 25 -o -p 1e-1 -y 2005

python production_SKiM.py data/prostateCancer_genes.txt data/B_terms_file_prostate_cancer.txt data/prostateCancer_drugs_TTDandDgidb.txt prostateCa_2010/ 25 -o -p 1e-2 -y 2010

python production_SKiM.py data/atherosclerosis_genes.txt data/B_terms_file_atherosclerosis.txt data/atherosclerosis_drugs_TTDandDgidb.txt atherosclerosis_full/ 25 -o -p 1e-7
