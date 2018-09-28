---
layout:     post
title:      Text-based large scale Search Engine 
subtitle:   Smarter people get more!
date:       2018-09-24
author:     Zhouyi
header-img: img/post-bg-entityclassify.jpg
catalog: true
tags:
    - Search Engine
    - Information Retrival
    - Natural Language Processing
    - Big Data
---

## OverView
	This is a search engine which helps people get information from a huge collection of documents. Users can simply type what they want and this machine returns several ranked related documents. Besides, a variety of advanced query operators are supported in this search engine like #NEAR, #WINDOW, #WSUM, #WOR and so on, this operators helps user specify their needs and get more satisfying documents.
  *The project is located [here](https://github.com/Zhouyiy/Entity_Classify)*

## Instruction
	For general search, directly input query in to query.txt
	For advanced search, firstly make up your structure query using operators below
  > | Operators| Instruction|
  > | ---- |:----:|
  > | #AND  | Return intersection of documents related to each of terms in query  |
  > | ---- |:----:|
  > | #OR   | Return union of documents related to each of terms in query|
  > | ---- |:----:|
  > | #NEAR/N| Return the documents in which query term B exists within N words after term A |
  > | ---- |:----:|
  > | #WINDOW/N | Return the documents in which term B exists within N words of term A|
  > | ---- |:----:|
  > | #WSUM | Attach each term of a weight, and return the best match documents|
  > | ---- |:----:|

  Sample queries:
  > #AND (apple, banana)
  
  > #OR (#NEAR/2(hedge fund), protected)

  > #WSUM ( 0.2 apple, 0.5 banana)

## Implementaion 
	It is a based on Lucene, and adopts DAAT(Document At A Time) structure which means no need to load all of the inverted list to memory. It supports which support a variety of retrieval models like Ranked Boolean/ Unranked Boolean/ BM25/ Indris retrieve models.

