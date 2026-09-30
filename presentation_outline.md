## Introduction Problem

### Why Decentralized Environments?
Decentralized environments have key advantages over the current decentralized nature of many aspects of current data storage solutions.

This is best explained with an example use-case. Note that this is just a singular with a narrow scope.

Current messaging applications tie an application to a single server, which only that application can use. 

Say you have a lot of friends who use different applications, you are forced to use them all to message all your friends.

This stifles innovation as aquiring the critical mass of users required to make people use your application is difficult and costly.

This is a direct result of vendor lock-in.

An alternative would be to create a decentralized environment where personal data stores are used to store message information. 

The application can then instead talk to the environment to obtain the data, thus decoupling data storage from the application used.

No more managing of multiple applications and promotes innovation in message applications features for example.


### How do we query them?
TODO: Makes slides for this part

These decentralized environments can be large, with many small sources full of privacy sensitive data that are not always known beforehand, how do we query this?

Link traversal is an iterative querying paradigm that discovers sources on the fly and is able to query sources on the document level.

These documents are resources at a given URI and are cheap to serve from a server perspective.

Link traversal enables granular access control and allows the query process to discover what sources to query using the follow your nose principle.


## Introduction Link Traversal

Just follow the slides

## Optimization Link Traversal

Link traversal is slow, partly due to lacking query optimization algorithms due to a lack of prior knowledge.

This is due to a lot of the different aspects of the data accessed depending on the query.
- Queried data
- Topology of the links between documents
- What documents are required to answer the query

To optimize the query there is the traditional query planning, such as join ordering

This is not the focus of our talk, instead we take a optimize-then-execute plan as a given, which is used to execute the query over our traversed documents

We instead focus on the traversal part of query execution and optimization

By default, link traversal uses a FIFO queue, corresponding to breadth-first traversal

We can instead optimize this by prioritizing documents required to answer the query, which intuitively should increase the arrival times of query results.

We can also prune documents from our traversal, however this requires some degree of prior knowledge about what documents definitely won't contribute

We won't focus on this, as we first want to investigate approaches that require no prior knowledge

## Problem Statement

Literature already contains some algorithms for prioritization, but they are tested on linked open data, which has significantly different topology and structure compared to 
structured decentralized environments.

Our goal is to investigate the performance of these algorithms in our new environment.

Problem:
- Implemented in an engine that is no longer maintained
- Measurements from original work include orthogonal design choices
- We need a baseline that measures marginal performance to serve as a basis for future research

## R3 Metric

First slide:
We introduce the R3 metric, a new tool for measuring prioritization performance
Introduce R3 metric according to the example

Second slide:
Definition 

Final Slide:
How do we find the optimal traversal path?
The traversed nodes act form a directed graph with root r.
The query-relevant documents can be seen as terminals to be visited in the graph
Thus, the problem is equivalent to steiner tree in directed graphs

## Data

TODO

## Algorithms

Just talk about algorithms tbh

## Results

Just talk


