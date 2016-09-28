[Taylor Berg-Kirkpatrick]: http://www.eecs.berkeley.edu/~tberg/
[Greg Durrett]: http://www.eecs.berkeley.edu/~gdurrett/
[Dan Klein]: http://www.eecs.berkeley.edu/~klein/
[Dan Garrette]: http://www.dhgarrette.com
[Hannah Alpert-Abrams]: http://www.halperta.com/



# OCR Evaluation Data

Authors: [Dan Garrette] and [Hannah Alpert-Abrams]

This is data that can be used to evaluate the Ocular historical document OCR system, which can be found here: https://github.com/tberg12/ocular.  It contains train/dev/test splits for several books, each with pre-extracted lines, and gold transcriptions for the dev and test sets.

Some subset of these documents were used for testing in the following publications:

> **Unsupervised Code-Switching for Multilingual Historical Document Transcription**
> [[pdf]](http://www.aclweb.org/anthology/N15-1109)    
> [Dan Garrette], [Hannah Alpert-Abrams], [Taylor Berg-Kirkpatrick], and [Dan Klein]  
> NAACL 2015

> **An Unsupervised Model of Orthographic Variation for Historical Document Transcription**
> [[pdf]](http://www.dhgarrette.com/papers/garrette_ocr_naacl2016.pdf)  
> [Dan Garrette] and [Hannah Alpert-Abrams]  
> NAACL 2016


If you find any mistakes in the gold transcriptions found in this repository, please let us know.  We would like for the transcriptions to be as accurate as possible.


### Running Ocular with the data

To train and evaluate with this data, use the following options during font training:

    -inputDocPath            documents/BOOK/train
    -extractedLinesPath      extractions/BOOK
    -evalInputDocPath        documents/BOOK/test
    -evalExtractedLinesPath  extractions/BOOK




### Retrieving image files

The actual page images are not stored in this repository.  Instead, the pre-extracted lines are.  However, all image files in `documents` can be found on the Primeros Libros website.  The urls for the images are formulaic, and can be determined from the image filename.  The filename template

    pl_LIBRARY_DOC_PAGE-1000.jpg

corresponds to the url template

    http://primeroslibros.org/page_view.php?id=pl_LIBRARY_DOC&lang=en&page=PAGE&view_single=1&zoom=1000

For example, the image for filename

    pl_jcbl_011_00024-1000.jpg

can be found at

    http://primeroslibros.org/page_view.php?id=pl_jcbl_011&lang=en&page=24&view_single=1&zoom=1000

