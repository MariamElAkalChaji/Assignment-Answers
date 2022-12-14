# Assignment 4
This assignment was made in collaboration with: Ana Karina Ballesteros Gómez, Ángela Gómez Sacristán, Mariam El Akal Chaji, Marta Fernández González and Paula Fernández Aldama.

It consists in the following:

Assignment: use of BLAST to Discover putative Orthologues

Orthologue DEFINITION: Genes that are found in different species that evolved from a common ancestral gene by speciation.

A common first-step in discovery of Orthologues is to do a “reciprocal best BLAST”. That is, you take protein X in Species A, and BLAST it against all proteins in Species B. The top (significant!!) hit in Species B is then BLASTed against all proteins in Species A. If it’s top (significant) hit is the Protein X, then those two proteins are considered to be Orthologue candidates. (there is more work to do after this, but this is a good start)

Using BioRuby to blast and parse the blast reports, find the orthologue pairs between species Arabidopsis and S. pombe. I have uploaded their complete proteomes to the Moodle for you. You do not need to create objects for this task (the existing BioRuby objects are sufficient)

To decide on "sensible" BLAST parameters, do a bit of online reading - when you have decided what parameters to use, please cite the paper or website that provided the information.

# Running the code

NOTE: First you will need to decompress TAIR10_cds_20101214_updated_1.fa.zip zip from the folder TAR10_cds_20101214_updated (it contains TAIR10_cds_20101214_updated_1.fa) - this is because the size of the fasta files that exceds the maximum allowed in GitHub.

In the terminal type: ruby Main.rb pep_1.fa TAIR10_cds_20101214_updated_1.fa

With this you will generate the Report.txt as the resulting report for this assignment.

# Other files
The other files corresponds with other databased files needed to found the ortologues between the two species.

In the folder /doc/ it is contained the Yard documentation for the code.

# Next steps in the analysis ...
To prove that the putative orthologues are truly orthologs, one would need to conduct further analyses.

After doing the reciprocal BLAST between this two species, we could compare them with homologous sequences from other species in order to determine if they form a monophyletic group.

Also another way to corroborate this information a sequence alignment can be used to compare the conserved domains between the sequences of both groups so we could see if there is a shared ancestry.

To top off this analysis we could analyze the expression patterns in both species to assure that they express similiary, thing that would provide more evidence if they are actually ortologues.

Another idea would be using metagenomic tools already implemented as eggNOG-Mapper (http://eggnog-mapper.embl.de/).

# Bibliography

General:

1. Blast local – Programación#Bioinformática. (s. f.). https://blogs.upm.es/estudiaciencia/blast-local/
2. BLAST search parameter E-value. (s. f.). http://insect-genome.com/blast/docs/e-value.html
3. Select all elements from one column in an array of arrays in Ruby? (2012, 27 julio). Stack Overflow. https://stackoverflow.com/questions/11688466/select-all-elements-from-one-column-in-an-array-of-arrays-in-ruby

For the parameters used in the code:

1. Hernández-Salmerón, J. E. & Moreno-Hagelsieb, G. (2020). Progress in quickly finding orthologs as reciprocal best hits: comparing blast, last, diamond and MMseqs2. BMC Genomics, 21(1). https://doi.org/10.1186/s12864-020-07132-6

For the "Next steps in analysis" :

1. Huerta-Cepas, J., Forslund, K., Coelho, L. P., Szklarczyk, D., Jensen, L. J., von Mering, C. & Bork, P. (2017). Fast Genome-Wide Functional Annotation through Orthology Assignment by eggNOG-Mapper. Molecular Biology and Evolution, 34(8), 2115-2122. https://doi.org/10.1093/molbev/msx148
2. Mylarshchikov, D. E. & Mironov, A. A. (2022). ortho2align: a sensitive approach for searching for orthologues of novel lncRNAs. BMC Bioinformatics, 23(1). https://doi.org/10.1186/s12859-022-04929-y
3. Nevers, Y., Jones, T. E. M., Jyothi, D., Yates, B., Ferret, M., Portell-Silva, L., Codo, L., Cosentino, S., Marcet-Houben, M., Vlasova, A., Poidevin, L., Kress, A., Hickman, M., Persson, E., Piližota, I., Guijarro-Clarke, C., Altenhoff, A., Bruford, E. A., Cosentino, S., . . . Altenhoff, A. (2022). The Quest for Orthologs orthology benchmark service in 2022. Nucleic Acids Research, 50(W1), W623-W632. https://doi.org/10.1093/nar/gkac330
