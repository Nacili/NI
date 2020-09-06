# NI
Projekat iz Naučnog Izračunavanja

# Tema - Određivanje podtipova Raka Dojke

* Skup podatka preuzet je sa https://www.cbioportal.org/study/summary?id=brca_metabric
* Rad koji prati skup podataka može se pogledati na https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4866047/

## Podaci
Prilikom preuzimanja sa navedenog linka, dobija se pristup navedenim setovima podataka:
* **data_clinical_patient.txt** - sadrži osnovne podatke o pacijentima
* **data_clinical_sample.txt** - sadrži podatke o uzorcima tkiva koji pripadaju pacijentima iz prethodno navedenog fajla
* **data_CNA.txt** - sadrži podatke o promeni u broju kopija gena odgovornih za (ne)razvitak raka dojke
* **data_expression_median.txt** - sadrži podatke o ekspresiji gore navedenih gena za sve uzorke tkiva
* **data_gene_matrix.txt** - sadrži spisak svih pacijenata (ne znam zašto su je nazvali gene_matrix kad ne odgovara nazivu)
* **data_mRNA_median_Zscores.txt** - sadrži za svaki uzorak z-skor ekspresije gena
* **data_mutations_extended.txt** - sadrži podatke o mutacijama gore navedenih gena
* **data_mutations_mskcc.txt** - slično kao prethodno, samo sa drugačijim atributima

Struktura fajlova je tabularna, tako da su svakom setu podataka ekstenzije promenjene sa .txt na .tsv ladi lakšeg baratanja sa podacima unutar fajlova. Svaki od navedenih fajlova ima svog meta para, koji mu opisuje sadržinu.

## Motivacija

Kod raka dojke postoji nekoliko podtipova same bolesti:
* claudin-low
* LuminalA
* LuminalB
* Her2 enriched
* Basal
* Normal

Svaki od ovih podtipova prima različitu terapiju i zato je jako bitno da možemo da ih razlikujemo. Ideja je da se pokuša sa integrativnim pristupom, tj. da se povežu podaci koji predstavljaju kliničku sliku sa genomskim podacima.

# Reference

* Claudin-Low Breast Cancer; Clinical & Pathological Characteristics: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5207440/
* Personalizing the treatment of women with early breast cancer: highlights of the St Gallen International Expert Consensus on the Primary Therapy of Early Breast Cancer 2013 https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3755334/
