
This repository contains the source code implementation of LibAdvisor, the dataset as well as the experimental results for the following paper:

<b>"A collaborative-filtering approach to provide OSS developers with third-party library recommendations"</b>


LibAdvisor is a framework that exploits cross projects relationships in open source software repositories to build a recommender system. It aims at supporting software developers who have already included some libraries in the new projects being developed, and expect to get recommendations on which additional libraries should be further incorporated. The LibAdvisor architecture is as follows:

<p align="center">
<img src="https://github.com/saner2019-libadvisor/LibAdvisor/blob/master/images/LibAdvisor.png" width="450">
</p>

The developer interacts with the system by sending a request for recommendations. The request contains a list of libraries that are already included in the project the developer is working on. The <b>Data Encoder</b> collects <i> background data </i> from OSS repositories, represents them in a <i>mathematically computable format</i>, which is then used as a base for other components of LibAdvisor.

The <b> Similarity Calculator</b> module computes similarities among projects to find the most similar ones to the given project. The <b>Recommendation Engine</b> gets the list of <i> top-k</i> similar projects and executes recommendation techniques to generate a ranked list of <i> top-N </i> libraries. Finally, the recommendations are sent back to the developer. Background data can be collected from different OSS platforms like GitHub, Eclipse, BitBucket. The current version of LibAdvisor supports data extraction from GitHub, even though the support for additional platforms is already under development.

LibAdvisor has been evaluated by considering different quality metrics and a dataset consisting of 1.200 GitHub Java projects. The performed evaluation demonstrated that our approach outperforms [LibRec](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6671293), a well-known system for library recommendation with regards to various quality indicators. To the best of our knowledge, our work is the first one that employs graphs to represent the relationships among software projects so as to effectively compute similarity and eventually to recommend libraries. 



There are the following main folders:

1. <b>experimental\_results</b> contains all the results obtained from the experiments with LibRec and LibAdvisor.

2. <b>tool</b>: Following the instruction provided in the folder, you can setup and run the source code using the dataset mentioned in the paper.
