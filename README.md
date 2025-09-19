# Connective Edits Dataset

A dataset of **connective edits (deleteions and replacements)** observed in the revision history of instructional texts from WikiHow.

---

##  Data Description

This dataset is based on the revision histories of WikiHow articles, extracted from the [wikiHowToImprove dataset](https://github.com/irshadbhat/wikiHowToImprove). WikiHow is a collaboratively edited platform offering step-by-step guides for everyday tasks, and each article contains a rich revision history created by various contributors.

**We use the same train/dev/test split as in the original `wikiHowToImprove` dataset**.

The dataset consists of two components:

### 1. WikiHow Connective Deletions

This part includes revisions in which a **discourse connective** (e.g., "However", "As a result") has been deleted at the beginning of a sentence, without any other changes between the original and revised versions. These insertions make previously explicit discourse relations implicit.

For each data split (i.e., **train**, **dev**, and **test**), the following TSV file is provided:

delete_connective_begin_{split}_with_context.tsv

Each file contains the following columns:

- `Article.Filename`: Name of the WikiHow article file  
- `Article.Original-section`: Section where the original sentence appears  
- `Sentence.Original`: The sentence before the revision  
- `Article.Revision-section`: Section where the revised sentence appears  
- `Sentence.Revision`: The sentence after the connective was deleted  
- `Sentence.Edits`: Type of edits made (in this case, deletion)  
- `Sentence.Context-before`: Text that precedes the revision  
- `Sentence.Context-after`: Sentence that follows the revision  

### 2. WikiHow Connective Replacements

This part includes revisions in which a **discourse connective** (e.g., "However", "As a result")  at the beginning of a sentence has been replaced with another connective, without any other changes between the original and revised versions.

For each data split (i.e., **train**, **dev**, and **test**), the following TSV file is provided:

insert_connective_begin_{split}_with_context.tsv

Each file contains the following columns:

- `Article.Filename`: Name of the WikiHow article file  
- `Article.Original-section`: Section where the original sentence appears  
- `Sentence.Original`: The sentence before the revision  
- `Article.Revision-section`: Section where the revised sentence appears  
- `Sentence.Revision`: The sentence after the connective was inserted  
- `Sentence.Edits`: Type of edits made (in this case, insertion)  
- `Sentence.Context-before`: Text that precedes the revision  
- `Sentence.Context-after`: Sentence that follows the revision  

## License

This dataset is distributed under the [Creative Commons Attribution-NonCommercial-ShareAlike 3.0 License (CC BY-NC-SA 3.0)](https://creativecommons.org/licenses/by-nc-sa/3.0/), in accordance with the licensing of the original WikiHow content.

---

## Contact

If you have any questions about this dataset, feel free to contact:

📧 **berfin.aktas@utn.de**

---

## Citation
If you use this dataset in your research, please cite the following paper:

**Berfin Aktaş and Michael Roth.** 2025. *Information-Theoretic and Prompt-Based Evaluation of Discourse Connective Edits in Instructional Text Revisions*. In Proceedings of the 6th Workshop on Computational Approaches to Discourse (CODI 2025). Association for Computational Linguistics.*(To appear)*

