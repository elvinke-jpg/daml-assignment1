# daml-assignment1
This repository checks that a Python environment works.
To run the notebook, clone this repository, go into its folder, and run:
```
conda create -n daml-test python=3.12
conda activate daml-test
pip install -r requirements.txt
jupyter notebook
```

1. Dataset:
   This dataset contains 20 poems selected from Poems by Currer, Ellis, and Acton Bell, published in 1846. The collection was published under the pseudonyms Currer, Ellis, and Acton Bell, which were used by Charlotte Brontë, Emily Brontë, and Anne Brontë.
   Each item in this dataset represents one individual poem, saved as separate .txt files. The dataset contains 20 poems in total. The original text of the complete book is preserved in the original_material folder.

2. Motivation:
   The purpose of this dataset it to make a small collection of nineteenth-century English poetry availalbe for research. The dataset can be used to research literary language, themes, vocabulary, and differences between poems.
   Possible research questions could be:
 - Which words and themes occur most frequently in the selected poems?
 - What similarities and differences can be found between the poems?
 - How are topics such as emotion represented in the poems?
 - Etc.

3. Selection criteria:
   The dataset consists of 20 poems selected from the 1846 collection Poems by Currer, Ellis, and Acton Bell. These poems are the first 20 poems mentioned in the collection.
   The dataset represetns a selection from one historical poetry collection. It does not represent all poetry written by the Brontë sisters or nineteenth-century English poetry in general. Poems outside the selected collection and poems from the collection not included in the selection are not represented.

4. Data collection process:
   The original book was obtained from the Internet Archive: https://archive.org/details/poemsbycurrerell00bron
   The full-text OCR version was downloaded and saved as poemsbybronte.txt in the original_material folder.
   The 20 selected poems were extracted manually from the original text and saved as seperate .txt files in the data folder.
   Date of collection: 2026-11-25

5. Cleaning and preprocessing:
   No additional cleaning or preprocessing was performed. The extracted poems retain the text of the original transcription, and are stored in the data folder. As a result, errors in the text may be present.

6. Structure:
   The repository is organised as follows:
   daml-assignment1/
       original_material/
            poemsbybronte.txt
   data/
      poem_001.txt
      poem_002.txt
      poem_003.txt
      ...
   data_cleaned/
      poem_001.txt
      poem_002.txt
      poem_003.txt
      ...
   metadata.csv
   check_dataset.ipynb
   check_environment.ipynb
   requirements.txt
   .gitignore
   README.md

   Metadata codebook:

   Column name:    Description:     Type:    Allowed values:     Missing values:
   -----------------------------------------------------------------------------------
   id              Identifier        String   001-020             Not allowed
                   assigned to
                   each poem

   file            Path to the       String   data/poem_001.txt,  Not allowed
                   original text              etc
                   file of the
                   poem

   source          Source from       URL      Internet Archive    Not allowed
                   which the poem             URL
                   was obtained

   licence         Copyright or      String   As stated by the    Unknown
                   reuse licence              source
                   information
                   for the source

   title           Title of the      String  Text as given in     Blank if 
                   poem                      the original         unavailable
                                             collection

   author          Author of the     String  Charlotte, Emily,    Blank if
                   poem                      or Anne Brontë       unavailable

   pseudonym       pseudonym name    String  Currer, Ellis,       Blank if
                   of author                 or Acton Bell        unavailable 

   year            Year of           String  1846                 Blank if
                   publication                                    unavailable

   pages           Page number or    String  12 or 12-14          Blank if 
                   page range of                                  unavailable
                   the poem in the
                   original
                   collection

7. Uses and limitations:
   The dataset can be used for small-scale text analysis. The texts are English-language poems from a nineteenth-century British literary collection published in 1846. The collection is associated with three female authors writing under pseudonyms.
   The dataset is limited to 20 selected poems from a single collection. It should not be treated as representative of all the Brontë sisters' writing or nineteenth-century literature as a whole. The book transcription may also contain errors that could affect computational text analysis.

8. Ethical and legal aspects:
   ccording to the Internet Archive's Terms of Use, individul materials may be subject to seperate copyright restrictions or licences. Therefore, the copyright and reuse conditions of the specific book collection should be considered sperately from the general Internet Archive Terms of Use.
   The dataset contains literary texts and does not intentionally contain personal information about living individuals. The dataset is shared for educational and research purposes. 

9. Licence and citation:
   The original book collection is identified as being available under a Creative Commons Attribution-ShareAlike (CC BY-SA) licence. This dataset follows the same licence.
   When using this dataset, please cite the original collection as well as the dataset's GitHub repository.
   Poems by Currer, Ellis, And Acton Bell (1846). Internet Archive: https://archive.org/details/poemsbycurrerell00bron