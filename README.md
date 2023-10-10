
## fastText with modified factored CBOW

## Table of contents

* [Introduction](#introduction)
* [Full documentation](#full-documentation)
* [References](#references)

## Introduction

## Full documentation

Invoke a command without arguments to list available arguments and their default values:

```
$ ./fasttext supervised
Empty input or output path.

The following arguments are mandatory:
  -input              training file path
  -output             output file path

The following arguments are optional:
  -verbose            verbosity level [2]

The following arguments for the dictionary are optional:
  -minCount           minimal number of word occurences [1]
  -minCountLabel      minimal number of label occurences [0]
  -wordNgrams         max length of word ngram [1]
  -bucket             number of buckets [2000000]
  -minn               min length of char ngram [0]
  -maxn               max length of char ngram [0]
  -t                  sampling threshold [0.0001]
  -label              labels prefix [__label__]
  -factored-delimiter factor delimiter prefix [0x04]

The following arguments for training are optional:
  -lr                 learning rate [0.1]
  -lrUpdateRate       change the rate of updates for the learning rate [100]
  -dim                size of word vectors [100]
  -ws                 size of the context window [5]
  -epoch              number of epochs [5]
  -neg                number of negatives sampled [5]
  -loss               loss function {ns, hs, softmax} [softmax]
  -thread             number of threads [12]
  -pretrainedVectors  pretrained word vectors for supervised learning []
  -saveOutput         whether output params should be saved [0]

The following arguments for quantization are optional:
  -cutoff             number of words and ngrams to retain [0]
  -retrain            finetune embeddings if a cutoff is applied [0]
  -qnorm              quantizing the norm separately [0]
  -qout               quantizing the classifier [0]
  -dsub               size of each sub-vector [2]
```

The website of the original fastText is located [*here*](https://github.com/facebookresearch/fastText)

## References for the fastText with factored CBOW
[0] Attila Novák, László Laki, Borbála Novák, [CBOW-tag: a Modified CBOW Algorithm for Generating Embedding Models from Annotated Corpora](https://aclanthology.org/2020.lrec-1.590/)
```
@inproceedings{novak-etal-2020-cbow,
    title = "{CBOW}-tag: a Modified {CBOW} Algorithm for Generating Embedding Models from Annotated Corpora",
    author = "Nov{\'a}k, Attila  and
      Laki, L{\'a}szl{\'o}  and
      Nov{\'a}k, Borb{\'a}la",
    booktitle = "Proceedings of the Twelfth Language Resources and Evaluation Conference",
    month = may,
    year = "2020",
    address = "Marseille, France",
    publisher = "European Language Resources Association",
    url = "https://aclanthology.org/2020.lrec-1.590",
    pages = "4798--4801",
    abstract = "In this paper, we present a modified version of the CBOW algorithm implemented in the fastText framework. Our modified algorithm, CBOW-tag builds a vector space model that includes the representation of the original word forms and their annotation at the same time. We illustrate the results by presenting a model built from a corpus that includes morphological and syntactic annotations. The simultaneous presence of unannotated elements and different annotations at the same time in the model makes it possible to constrain nearest neighbour queries to specific types of elements. The model can thus efficiently answer questions such as What do we eat?, What can we do with a skeleton? What else do we do with what we eat?, etc. Error analysis reveals that the model can highlight errors introduced into the annotation by the tagger and parser we used to generate the annotations as well as lexical peculiarities in the corpus itself, especially if we do not limit the vocabulary of the model to frequent items.",
    language = "English",
    ISBN = "979-10-95546-34-4",
}
```

## References from the original fastText

Please cite [1](#enriching-word-vectors-with-subword-information) if using this code for learning word representations or [2](#bag-of-tricks-for-efficient-text-classification) if using for text classification.

### Enriching Word Vectors with Subword Information

[1] P. Bojanowski\*, E. Grave\*, A. Joulin, T. Mikolov, [*Enriching Word Vectors with Subword Information*](https://arxiv.org/abs/1607.04606)

```
@article{bojanowski2017enriching,
  title={Enriching Word Vectors with Subword Information},
  author={Bojanowski, Piotr and Grave, Edouard and Joulin, Armand and Mikolov, Tomas},
  journal={Transactions of the Association for Computational Linguistics},
  volume={5},
  year={2017},
  issn={2307-387X},
  pages={135--146}
}
```

### Bag of Tricks for Efficient Text Classification

[2] A. Joulin, E. Grave, P. Bojanowski, T. Mikolov, [*Bag of Tricks for Efficient Text Classification*](https://arxiv.org/abs/1607.01759)

```
@InProceedings{joulin2017bag,
  title={Bag of Tricks for Efficient Text Classification},
  author={Joulin, Armand and Grave, Edouard and Bojanowski, Piotr and Mikolov, Tomas},
  booktitle={Proceedings of the 15th Conference of the European Chapter of the Association for Computational Linguistics: Volume 2, Short Papers},
  month={April},
  year={2017},
  publisher={Association for Computational Linguistics},
  pages={427--431},
}
```

### FastText.zip: Compressing text classification models

[3] A. Joulin, E. Grave, P. Bojanowski, M. Douze, H. Jégou, T. Mikolov, [*FastText.zip: Compressing text classification models*](https://arxiv.org/abs/1612.03651)

```
@article{joulin2016fasttext,
  title={FastText.zip: Compressing text classification models},
  author={Joulin, Armand and Grave, Edouard and Bojanowski, Piotr and Douze, Matthijs and J{\'e}gou, H{\'e}rve and Mikolov, Tomas},
  journal={arXiv preprint arXiv:1612.03651},
  year={2016}
}
```

(\* These authors contributed equally.)
