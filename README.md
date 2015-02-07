# dupfile-scanner
Scan the disk and list the duplicate file.
Need to scan and calculate the md5 for all the files you choose at the first time. And will do incremental scan after that. 
##How it works
###First time scan
1. Scan all the files with the extension you choose.
2. Calculate the md5 for all the files and write a .hashfile.md5 for each directory.
3. List all the duplicate files.
###Incremental scan
Use makefile to generate .hashfile.md5 incrementally. Only update the .hashfile.md5 once any file in this folder was changed after the .hashfile.md5 generated.
So it will only calcuate the md5 for new added files.
