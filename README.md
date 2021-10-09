# NLP Sentiment-Analysis with BERT

The data for this project was taken from the twitter [SMILE](https://figshare.com/articles/dataset/smile_annotations_final_csv/3187909/2) dataset. 
It contains 3,085 tweets, with 5 emotions namely anger, disgust, happiness, surprise and sadness. Please see our paper "SMILE: Twitter Emotion Classification using Domain Adaptation" for more details of the dataset.

```
> df.head()


id:	          text:	                                            category:	
6.121680e+17	@stiveshouse @MillenniumArt @Tate_StIves @Trem...	happy
6.116340e+17	I miss Cornwall so much. #ff @FernPitCafe @Pen...	not-relevant
6.107630e+17	£10 off @accessart http://t.co/0biFQaXTQg memb...	not-relevant
6.115290e+17	@britishmuseum @Ophiolatrist Spain? Egypt?	nocode
6.151070e+17	Enjoying the amazing collections @britishmuseu...	happy
```
```
> df.category.value_counts()

nocode               1554
happy                1123
not-relevant          211
angry                  56
surprise               35
sad                    32
happy|surprise         11
happy|sad               9
disgust|angry           7
disgust                 6
sad|disgust             2
sad|angry               2
sad|disgust|angry       1
```
<br/>

# BERT Architecture

"**B**idirectional **E**ncoder **R**epresentations from **T**ransformers" or BERT is a 
pre-trained deep learning model introduced in a [recent paper](https://arxiv.org/pdf/1810.04805.pdf) from Google. 
The model leverages conditional probability on both left and right (preceeding & proceeding) words in a text. Used to create machine language comprehension models.

![cover_photo](BERT_diagrams.png)


# Assessing model accuracy by claass
```
> accuracy_per_class(predictions, true_vals)

Class: happy
Accuracy: 248/251

Class: not-relevant
Accuracy: 29/51

Class: angry
Accuracy: 5/15

Class: disgust
Accuracy: 0/2

Class: sad
Accuracy: 0/8

Class: surprise
Accuracy: 0/11
```
