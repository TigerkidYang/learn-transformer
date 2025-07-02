# Learn Transformer

This repository will contain some stuff I build as exercise when studing Transformer.

## nano-GPT

A Transformer-based stylistic text generation model

### Tech Stack

Python, PyTorch, Transformer, Natural Language Processing (NLP)

### Description

- Implemented a character-level language model based on Transformer architecture, aimed at learning and generating text that mimics the style of `input.txt`.

- Started with data preprocessing, including building vocabulary, data splitting, and batch processing

- Adopted modular programming by encapsulating attention heads (Head), multi-head attention (Multi-Head Attention), and Transformer blocks (Block) as independent `PyTorch nn.Module`, improving code readability and extensibility

- Implemented a Decoder-only Transformer architecture, fully implementing key modules of the Transformer model including token embedding, positional embedding, multi-head self-attention mechanism, residual connection & layer normalization, and feed-forward network

- Quantitatively evaluated model performance through training loss and validation loss

- The final model achieved a loss of 1.47 on the validation set and successfully generated text with similar formatting, although semantically incoherent but capable of generating correct words

### Results

```
step 0: train loss 4.2849, val loss 4.2823
step 500: train loss 2.0077, val loss 2.0954
step 1000: train loss 1.5929, val loss 1.7706
step 1500: train loss 1.4384, val loss 1.6420
step 2000: train loss 1.3394, val loss 1.5739
step 2500: train loss 1.2769, val loss 1.5330
step 3000: train loss 1.2263, val loss 1.5067
step 3500: train loss 1.1843, val loss 1.4901
step 4000: train loss 1.1470, val loss 1.4858
step 4500: train loss 1.1100, val loss 1.4769
```

```
You had, if rudes are forth, reputation of you:
You, my great day, we have write own to bloody;
And 'twixt you, by any hung.

DUKE VINCENTIO:
Hard you that from the deafter.

ROMEO:
Shalt show the carce: the glore is wly to encounter'd
In soldiercretess slain for and what news? Or dills she
Hath slept the rock from shelB herself.

Provost:
Soft, that sovereign both.

DUCHESS OF YORK:
As sweet we will cobillo me with my son.

HENRY ROMEOND:
O Walton, alas! that's that I draw on me.

SAMPSON:
Why,
```

可以看见生成的文本具有类似`input.txt`中的莎士比亚戏剧的格式。而且，虽然仔细读起来完全牛头不对马嘴，但已经开始是由现实存在的单词组成的东西了。