# SentencePairMatch_doc2vec-word2vec
基于Doc2vec和Word2vec的句子对匹配方法
句子对匹配（Sentence Pair Matching）问题是NLP中非常常见的一类问题，所谓“句子对匹配”，就是说给定两个句子S1和S2，任务目标是判断这两个句子是否具备某种类型的关系。本项目是一个Word2vec和Doc2vec的应用，使用Word2vec和Doc2vec得到句子的向量表示，然后计算cosin相似度，并在Quora公开的一个数据集上做了一些对比试验，是一种无监督的句子对匹配方法。具体可以参考我的博客：

其中，train_doc2vector_model.py和train_word2vec_model.py是训练doc2vec和Word2vec模型的代码，使用了Gensim库。train_doc2vector_model.py既可以训练doc2vec，也可以训练Word2vec；

ParaPhrase_doc2vec.py是使用doc2vec得到句子的向量表示，然后进行相似度计算；

ParaPhrase_word2vec.py是使用句子中词的Word2vec相加求均值得到句子的向量表示，然后进行相似度计算；

eval.py对相似度计算的结果与语料库标注结果做对比，计算准确率。
