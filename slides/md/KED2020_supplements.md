---
title: The ABC of computational Text Analysis
subtitle: "Supplements"
author: "Alex Flückiger"
institute: |
  | Faculty of Humanities and Social Sciences
  | University of Lucerne
date: "23 April 2020"
lang: en-US
---



## Purpose

Here I present some stuff that we did not cover in class.

## Tasks

- find various ngrams with wildcards
- check gender specific language
  - what follows `she/he` or `her/his`





## Key Word in Context (KWIC)

```bash
ptx -f -w 50 */*.txt > ptx.txt
egrep -i "[a-z]  word" ptx.txt
```



## Select Column in Dataset

```bash
cut -d\t -f1 	# extract the 2nd column from a tab-separated file
```



## Extract texts from tsv: 

* http://www.theunixschool.com/2012/05/shell-read-text-or-csv-file-and-extract.html 

## Variables

```bash
echo "Starting program at $(date)" 
```



## Batch Processing

```bash
for file in *.txt; do			# loop over all text files
 cat "$file" | pipe commands > "proc_$file"
done
```





## Batch Renaming

```bash
rename  " " "_" *.txt	# replace spaces with underscores
# since there are different versions, if this doesn't work try:
# rename 's/ /_/' *.txt

```

```bash
i=1
for file in *.txt; do			# loop over all text files
 mv -- "$file" "text_$i.txt"	# rename each file with a sequential number
 i=$((i+1))
done
```



## Data Cleaning



## In-class: Exercises I{data-background=#3c70b5}



