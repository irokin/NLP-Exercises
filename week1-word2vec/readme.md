# Word2vec

Week 1 exercise is about understanding the intuition and architecture of word2vec. Specifically:
- preprocess the datasets posted in the 
[automatic summarization and reasoning competition](https://aistudio.baidu.com/aistudio/competition/detail/3) into a corpus
- generate a vocabulary list and a collection of sentences from the corpus
- use gensim's implementation of [word2vec](https://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and-their-compositionality.pdf) to learn word embeddings

## Discussion
The intuition of word2vec is that semantically similar words tend to be near to each other, which translates to maximize the conditional probability of observing the target word (context words) given the context words (target word) when CBOW (skip-gram) is employed. For detailed discussion, please refer to this [tutorial](https://arxiv.org/pdf/1411.2738.pdf). Also, an interactive [demo](https://ronxin.github.io/wevi/) that visualize the training process. 

One debating point that leads to the publications of a number of papers is the representation of the final word embedding. As both input and output weight matrices contain embeddings for the same set of words, different strategies, including average, concatenation, sum or max the input and output embeddings of the same words, have been proposed. For detailed discussion, please refer to this [paper](https://www.aclweb.org/anthology/W15-1513.pdf).