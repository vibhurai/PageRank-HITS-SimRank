Info:

-> Dataset me links.txt name ki file h, thats our data.

-> /src has diff files out of which Graph.py is responsible for converting the raw data to a graph. Skim through this file once to see all the functions that the program uses over the course of its execution.

-> HTIS is working perfectly, Simrank isn't necessary ig, Pagerank tum log samajhkr ek baar crosscheck krlna if the guy's code is in accordance with the algorithm or not.

-> The /results would have a filder for each datasert which would further have texts files with the pageranking, auth and hub scores for the dataset.

-> /img is unnecessary. main.py is where the program is mainly executed from.

-> As of now, the things left to do are....

    > Understanding pageranking working
    > Implementing and making query processing for link analysis algos and incorporating the same
    > Implementing VSM
    > Std metrics comparison bw link analysis algos and VSM

https://amitness.com/2020/08/information-retrieval-evaluation/


<p align=center>
    <img src="img/graph_4.png">
</p>

<p align=center>
    <a target="_blank" href="https://travis-ci.com/chonyy/AI-basketball-analysis" title="Build Status"><img src="https://travis-ci.com/chonyy/AI-basketball-analysis.svg?branch=master"></a>
    <a target="_blank" href="#" title="language count"><img src="https://img.shields.io/github/languages/count/chonyy/PageRank-HITS-SimRank"></a>
    <a target="_blank" href="#" title="top language"><img src="https://img.shields.io/github/languages/top/chonyy/PageRank-HITS-SimRank?color=orange"></a>
    <a target="_blank" href="https://opensource.org/licenses/MIT" title="License: MIT"><img src="https://img.shields.io/badge/License-MIT-blue.svg"></a>
    <a target="_blank" href="#" title="repo size"><img src="https://img.shields.io/github/repo-size/chonyy/PageRank-HITS-SimRank"></a>
    <a target="_blank" href="http://makeapullrequest.com" title="PRs Welcome"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg"></a>
</p>

> 🎏 Python implementation of famous link analysis algorithms.

I have written three articles to explain the concept and implementation of these three algorithms. Feel free to click on the link!

- [HITS Algorithm](https://towardsdatascience.com/hits-algorithm-link-analysis-explanation-and-python-implementation-61f0762fd7cf)
- [PageRank Algorithm](https://towardsdatascience.com/pagerank-3c568a7d2332)
- [SimRank Algorithm](https://towardsdatascience.com/simrank-similarity-analysis-1d8d5a18766a)
- [Evaluation Metrics](https://amitness.com/2020/08/information-retrieval-evaluation/)

## 💻 Getting Started

Get a copy of this repo using git clone
```
git clone https://github.com/chonyy/PageRank-HITS-SimRank.git
```

Run the program with dataset provided and **default** values for *damping_factor* = 0.15, *decay_factor* = 0.9 and *iteration* = 100

```
python main.py -f 'dataset/graph_1.txt'
```

Run program with dataset and cusotm parameters

```
python main.py --input_file 'dataset/graph_1.txt' --damping_factor 0.15 --decay_factor 0.9 --iteration 500
```

## Result

### Output on console

<p align=center>
    <img src="img/output.PNG">
</p>

The order of the result follows the order of the node value. For example, `1, 2, 5, 7`.

### Output to files in result folder

<p align=center>
    <img src="img/result.PNG">
</p>

A new folder with the name same with the graph will be created in the result directory. Four txt files will be created to store the value printed on the console.

- graph_HITS_authority.txt
- graph_HITS_hub.txt
- graph_PageRank.txt
- graph_SimRank.txt

## Analysis

<p align=center>
    <img src="img/convergence.png">
    <img src="img/HITS_nodetime.png">
    <img src="img/pagerank_node_time.png">
    <img src="img/simrank_nodetime.png">
</p>
