If you have a scanner with a document feeder that generates PDF files, but only scans one side of the pages, this utility is for you.  Instructions for use:

* Scan the front sides to one file.
* Flip the stack of papers over, and scan the back sides. (You will scan the last page first.)
* Run the pdfmergescan script to extract the individual pages, rearrange them in order, and combine them into a single PDF file.

``` sh
$ ./pdfmergescan front.pdf back.pdf -o combined.pdf
```

If the last page is blank, you may want to use the --skip-last option:

``` sh
$ ./pdfmergescan --skip-last front.pdf back.pdf -o combined.pdf
```

This will result in a PDF file with an odd number of pages.
