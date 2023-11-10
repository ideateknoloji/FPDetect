# FPDetect
Windows and Linux Based Applications of Filtering SNVs using Genomic Features and Quality Metrics



Filtering SNPs using Genomic Features and Quality Metrics

USAGE:
This is a command-line application so please open cmd (or terminal for linux)

WINDOWS: false_positive_scorer_win.exe -i[--input] input.csv -o[--output] output.csv

LINUX: Before using this program in Linux, find the directory where the program is located
in terminal environment and run the following command: chmod +x false_positive_scorer_linux
Then you are free to use false positive scorer with following command:

```
./false_positive_scorer_linux -i [--input] input.csv -o [--output] output.csv
```
-o(--output) parameter is optional. When output file path is not given, the program automatically create csv named as "results_YYYY_MM_DD_hh-mm-ss.csv" to current directory that the program runs.

SAMPLE FILE :
This csv file is annotated obtained from raw vcf file. Here, we leave the implementation
of the intermediate program to the user (program with which the csv containing the necessary annotations is obtained from the vcf). The desired format can be created using an annotation tool such as VEP.
We shared an example input csv file. You will see the formatted csv named as "proper_example_variants.csv". We also shared the ground truth for the false/true
positive classes of the variants in the "proper_example_variants_identifiers.csv". After you run
the program you can compare the actual classes and the predicted ones .

The following are example commands using this csv file:

WINDOWS:
```
false_positive_scorer_win.exe -i proper_example_variants.csv -o output.csv
```
```
false_positive_scorer_win.exe -i[--input] input.csv -o[--output] output.csv 
```

LINUX:
```
./false_positive_scorer_linux -i proper_example_variants.csv -o output.csv
```
```
./false_positive_scorer_linux -i[--input] input.csv -o[--output] output.csv
```

This application is licenced with Creative Commons Corporation and for commercial use please contact; kvnceren@gmail.com, hukarakurt@gmail.com and cinaresra@yahoo.com
