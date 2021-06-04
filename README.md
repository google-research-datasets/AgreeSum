# AgreeSum Dataset

This repository contains the raw dataset used for the agreement-oriented
multi-doc summarization (AgreeSum) task from ["AgreeSum: Agreement-Oriented
Multi-Document Summarization"]() to appear in the Findings of the ACL:
ACL-IJCNLP 2021.

The dataset consists of summaries from Wikipedia Current Events Portal (WCEP),
along with associated news article URLs (up to four) and whether or not the
summary entails the main passage of each news article. Entailment here is
defined as "Does the article contain all the information presented in the
summary?" The dataset consists of 18K cluster-summary pairs, coming from
5.5K WCEP summaries. 1K cluster-summary pairs are annotated, which corresponds
to ~8K article-summary entailment annotations.

This dataset may be alternatively flattened, deduplicated, and used in a
(summary, article) entailment classification setting.

## Dataset Construction

For more details on how the dataset is constructed, please refer to our paper.

## Important Notes
- The summaries provided in the test set are *not* gold summaries, as test set
  articles are not guaranteed to entail the summary. However, these summaries
  may be used as a proxy to measure summarizaiton informativeness.
- The dev set is sampled from the training set, which comes from WCEP summaries
  before August 2019, while the test set is from August 2019 to August 2020.
- Entailment labels have four possible values: 1 (entails), 0 (not entails), -1
  (unannotated), and -2 (no article at that position).

# Citation
If you use or discuss this dataset in your work, please cite our paper:

```
@InProceedings{agreesum2021,
  title = {{AgreeSum: Agreement-Oriented Multi-Document Summarization}},
  author = {Richard Yuanzhe Pang, Adam D. Lelkes, Vinh Q. Tran and Cong Yu},
  booktitle = {Findings of the ACL: ACL-IJCNLP 2021},
  year = {2021}
}
```
