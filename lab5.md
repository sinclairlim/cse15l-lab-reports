This report is a writeup about researching the command, "find". 

Source: 
[tecmint](https://www.tecmint.com/35-practical-examples-of-linux-find-command/), [linuxconfig](https://linuxconfig.org/how-to-use-find-command-to-search-for-files-based-on-file-size), [alvinalexander](https://alvinalexander.com/unix/edu/examples/find.shtml)

**Command 1: Name, -name** 
<br>
This command find all the files in the current directory that matches the search. 

Example: "WhereToItaly"
```
[cs15lwi23agz@ieng6-203]:berlitz1:284$ find . -name WhereToItaly.txt
./WhereToItaly.txt
```

This example shows that only one file matches "WhereToItaly.txt" in the current working directory.

Example: "WhereToHongKong"
```
[cs15lwi23agz@ieng6-203]:berlitz1:285$ find . -name WhereToHongKong.txt
./WhereToHongKong.txt
```

This example shows that only one file matches "WhereToHongKong.txt" in the current working directory.

**Command 2: Size , -size** 

This command searches for files within a specific size range.

Example: files below 2MB
```
[cs15lwi23agz@ieng6-203]:berlitz1:300$ find . -size -2M
.
./HandRHawaii.txt
./HandRHongKong.txt
./HandRIbiza.txt
./HandRIsrael.txt
./HandRIstanbul.txt
./HandRJamaica.txt
./HandRJerusalem.txt
./HandRLakeDistrict.txt
./HandRLasVegas.txt
./HandRLisbon.txt
./HandRLosAngeles.txt
./HandRMadeira.txt
./HandRMadrid.txt
./HandRMallorca.txt
./HistoryDublin.txt
./HistoryEdinburgh.txt
./HistoryEgypt.txt
./HistoryFWI.txt
./HistoryFrance.txt
./HistoryGreek.txt
./HistoryHawaii.txt
./HistoryHongKong.txt
./HistoryIbiza.txt
./HistoryIndia.txt
./HistoryIsrael.txt
./HistoryIstanbul.txt
./HistoryItaly.txt
./HistoryJamaica.txt
./HistoryJapan.txt
./HistoryJerusalem.txt
./HistoryLakeDistrict.txt
./HistoryLasVegas.txt
./HistoryMadeira.txt
./HistoryMadrid.txt
./HistoryMalaysia.txt
./HistoryMallorca.txt
./IntroDublin.txt
./IntroEdinburgh.txt
./IntroEgypt.txt
./IntroFWI.txt
./IntroFrance.txt
./IntroGreek.txt
./IntroHongKong.txt
./IntroIbiza.txt
./IntroIndia.txt
./IntroIsrael.txt
./IntroIstanbul.txt
./IntroItaly.txt
./IntroJamaica.txt
./IntroJapan.txt
./IntroJerusalem.txt
./IntroLakeDistrict.txt
./IntroLasVegas.txt
./IntroLosAngeles.txt
./IntroMadeira.txt
./IntroMadrid.txt
./IntroMalaysia.txt
./IntroMallorca.txt
./JungleMalaysia.txt
./WhatToDublin.txt
./WhatToEdinburgh.txt
./WhatToEgypt.txt
./WhatToFWI.txt
./WhatToFrance.txt
./WhatToGreek.txt
./WhatToHawaii.txt
./WhatToHongKong.txt
./WhatToIbiza.txt
./WhatToIndia.txt
./WhatToIsrael.txt
./WhatToIstanbul.txt
./WhatToItaly.txt
./WhatToJamaica.txt
./WhatToJapan.txt
./WhatToLakeDistrict.txt
./WhatToLasVegas.txt
./WhatToLosAngeles.txt
./WhatToMadeira.txt
./WhatToMalaysia.txt
./WhatToMallorca.txt
./WhereToDublin.txt
./WhereToEdinburgh.txt
./WhereToEgypt.txt
./WhereToFWI.txt
./WhereToFrance.txt
./WhereToGreek.txt
./WhereToHawaii.txt
./WhereToHongKong.txt
./WhereToIbiza.txt
./WhereToIndia.txt
./WhereToIsrael.txt
./WhereToIstanbul.txt
./WhereToItaly.txt
./WhereToJapan.txt
./WhereToJerusalem.txt
./WhereToLakeDistrict.txt
./WhereToLosAngeles.txt
./WhereToMadeira.txt
./WhereToMadrid.txt
./WhereToMalaysia.txt
./WhereToMallorca.txt```

The files displayed are files that are below 2MB in size.

Example: files above 100KB
```
[cs15lwi23agz@ieng6-203]:berlitz1:304$ find . -size +100k
./WhereToFrance.txt
./WhereToIndia.txt
./WhereToItaly.txt
./WhereToJapan.txt
./WhereToMalaysia.txt```

The files displayed are files that are above 100KB in size.

**Command 3: Type , -type** 

This command finds the types of files only as specified.

Example: finding files only
```
[cs15lwi23agz@ieng6-203]:berlitz1:305$ find . -type f
./HandRHawaii.txt
./HandRHongKong.txt
./HandRIbiza.txt
./HandRIsrael.txt
./HandRIstanbul.txt
./HandRJamaica.txt
./HandRJerusalem.txt
./HandRLakeDistrict.txt
./HandRLasVegas.txt
./HandRLisbon.txt
./HandRLosAngeles.txt
./HandRMadeira.txt
./HandRMadrid.txt
./HandRMallorca.txt
./HistoryDublin.txt
./HistoryEdinburgh.txt
./HistoryEgypt.txt
./HistoryFWI.txt
./HistoryFrance.txt
./HistoryGreek.txt
./HistoryHawaii.txt
./HistoryHongKong.txt
./HistoryIbiza.txt
./HistoryIndia.txt
./HistoryIsrael.txt
./HistoryIstanbul.txt
./HistoryItaly.txt
./HistoryJamaica.txt
./HistoryJapan.txt
./HistoryJerusalem.txt
./HistoryLakeDistrict.txt
./HistoryLasVegas.txt
./HistoryMadeira.txt
./HistoryMadrid.txt
./HistoryMalaysia.txt
./HistoryMallorca.txt
./IntroDublin.txt
./IntroEdinburgh.txt
./IntroEgypt.txt
./IntroFWI.txt
./IntroFrance.txt
./IntroGreek.txt
./IntroHongKong.txt
./IntroIbiza.txt
./IntroIndia.txt
./IntroIsrael.txt
./IntroIstanbul.txt
./IntroItaly.txt
./IntroJamaica.txt
./IntroJapan.txt
./IntroJerusalem.txt
./IntroLakeDistrict.txt
./IntroLasVegas.txt
./IntroLosAngeles.txt
./IntroMadeira.txt
./IntroMadrid.txt
./IntroMalaysia.txt
./IntroMallorca.txt
./JungleMalaysia.txt
./WhatToDublin.txt
./WhatToEdinburgh.txt
./WhatToEgypt.txt
./WhatToFWI.txt
./WhatToFrance.txt
./WhatToGreek.txt
./WhatToHawaii.txt
./WhatToHongKong.txt
./WhatToIbiza.txt
./WhatToIndia.txt
./WhatToIsrael.txt
./WhatToIstanbul.txt
./WhatToItaly.txt
./WhatToJamaica.txt
./WhatToJapan.txt
./WhatToLakeDistrict.txt
./WhatToLasVegas.txt
./WhatToLosAngeles.txt
./WhatToMadeira.txt
./WhatToMalaysia.txt
./WhatToMallorca.txt
./WhereToDublin.txt
./WhereToEdinburgh.txt
./WhereToEgypt.txt
./WhereToFWI.txt
./WhereToFrance.txt
./WhereToGreek.txt
./WhereToHawaii.txt
./WhereToHongKong.txt
./WhereToIbiza.txt
./WhereToIndia.txt
./WhereToIsrael.txt
./WhereToIstanbul.txt
./WhereToItaly.txt
./WhereToJapan.txt
./WhereToJerusalem.txt
./WhereToLakeDistrict.txt
./WhereToLosAngeles.txt
./WhereToMadeira.txt
./WhereToMadrid.txt
./WhereToMalaysia.txt
./WhereToMallorca.txt
```


This lists shows all the files in the current working directory. 

Example: finding directories only
```
[cs15lwi23agz@ieng6-203]:berlitz1:306$ find . -type d
.
```

This shows that there are no directories in the current working directory. 

**Command 4: Not , -not** 

This command searches for files that do not match a pattern.

Example: Find text files that does not start with "W"
```
[cs15lwi23agz@ieng6-203]:berlitz1:316$ find . -not -name "W*.txt"
.
./HandRHawaii.txt
./HandRHongKong.txt
./HandRIbiza.txt
./HandRIsrael.txt
./HandRIstanbul.txt
./HandRJamaica.txt
./HandRJerusalem.txt
./HandRLakeDistrict.txt
./HandRLasVegas.txt
./HandRLisbon.txt
./HandRLosAngeles.txt
./HandRMadeira.txt
./HandRMadrid.txt
./HandRMallorca.txt
./HistoryDublin.txt
./HistoryEdinburgh.txt
./HistoryEgypt.txt
./HistoryFWI.txt
./HistoryFrance.txt
./HistoryGreek.txt
./HistoryHawaii.txt
./HistoryHongKong.txt
./HistoryIbiza.txt
./HistoryIndia.txt
./HistoryIsrael.txt
./HistoryIstanbul.txt
./HistoryItaly.txt
./HistoryJamaica.txt
./HistoryJapan.txt
./HistoryJerusalem.txt
./HistoryLakeDistrict.txt
./HistoryLasVegas.txt
./HistoryMadeira.txt
./HistoryMadrid.txt
./HistoryMalaysia.txt
./HistoryMallorca.txt
./IntroDublin.txt
./IntroEdinburgh.txt
./IntroEgypt.txt
./IntroFWI.txt
./IntroFrance.txt
./IntroGreek.txt
./IntroHongKong.txt
./IntroIbiza.txt
./IntroIndia.txt
./IntroIsrael.txt
./IntroIstanbul.txt
./IntroItaly.txt
./IntroJamaica.txt
./IntroJapan.txt
./IntroJerusalem.txt
./IntroLakeDistrict.txt
./IntroLasVegas.txt
./IntroLosAngeles.txt
./IntroMadeira.txt
./IntroMadrid.txt
./IntroMalaysia.txt
./IntroMallorca.txt
./JungleMalaysia.txt```

We can see that none of the results include text files that starts with "W".

Example: Find text files that does not have the alphabet "A" in the middle of their file name

```
[cs15lwi23agz@ieng6-203]:berlitz1:317$ find . -not -name "*a*.txt"
.
./HistoryDublin.txt
./HistoryEdinburgh.txt
./HistoryEgypt.txt
./HistoryFWI.txt
./HistoryGreek.txt
./HistoryHongKong.txt
./IntroDublin.txt
./IntroEdinburgh.txt
./IntroEgypt.txt
./IntroFWI.txt
./IntroGreek.txt
./IntroHongKong.txt
./IntroLosAngeles.txt
./WhereToDublin.txt
./WhereToEdinburgh.txt
./WhereToEgypt.txt
./WhereToFWI.txt
./WhereToGreek.txt
./WhereToHongKong.txt
./WhereToLosAngeles.txt
```

We can see that the none of the results include the alphabet "A".
