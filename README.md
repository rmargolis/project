# Gene Sequencing Comparison for Two Species
>Version 1.0

>December 2017

>The image for the function was taken from: https://www.yourgenome.org/facts/how-do-you-find-out-the-significance-of-a-genome-after-sequencing

## Functions Included in this Package
> Before running this program, you must first download the biopython software. This will be downloaded 
through conda. Enter the following into the command line of your terminal:

**conda install -c anaconda biopython** 

If you need to install conda, follow this link below and it will guide you to download it for either
Macintosh or Windows and update it to its current version.

https://conda.io/docs/user-guide/install/macos.html

>**ensembl_download.py**
This python script takes in the user inputs of species1 and genesymbol to generate a python dictionary using a json decoder.

>**loadfile_datebase.py**
This python script uses the user inputs of species 1 and genesymbol and generates a sqlite database from the python dictionary generated from the ensembl_download.py. The function outputs the database into a file titled "proteinsequenceDB.db.

>**seqparse.py**
This python script uses the species2 user input and reconnects back into the generate database, finding the target and source sequences associated with the species2 that the user chose. It then calculates the correlation between those two sequences and returns a percent. The higher the percent, a higher correlation of similarity.

>**genecomparison.php**
This php script helps provide a interface for the user to interact with the python scripts. The user inputs species1, genesymbol, and species2 and is outputed a percent correlation factor.
