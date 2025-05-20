# Detection-of-Hallucination-in-Arabic

This project aims to detect hallucinations ( nonfactcal answers) in Arabic Large Language Models (LLMs) using a Question-Answering dataset. The process involves generating answers, grouping similar answers, and testing methods to identify unreliable responses.

## repository structure:

Detection-of-Hallucination-in-Arabic/
├── Alloutput_files/           # Output files from experiments
├── Final-Experiment/          # Files related to the final experiment
├── data_set_code/             # Code for dataset exploring
├── our framework code/        # Implementation of our hallucination detection framework
└── README.md                  # Project documentation

## Features

Arabic-specific hallucination detection
Support for multiple LLM 
Quantitative metrics for hallucination assessment
Detailed analysis reports

## Steps

### 1 Generation
Our experimental procedures aim to detect hallucination in Arabic LLMs. for starter, up to 10 answers for each question from a specified dataset will be generated using the Llama suite models.  

### 2 Clustering
We also will experiment with various entailment models to identify the most suitable model for the semantic clustering step in our project. By evaluating multiple models, we aim to identify the one that best captures nuanced relationships within the answers generated for each question. This experimentation will involve assessing each model’s ability to accurately determine entailment and non-entailment across different text pairs. Our goal is to choose a model that enhances the clustering process, allowing us to group semantically related elements in a way that is both meaningful and reflective of subtle contextual relationships.

### 3 Baseline and semantic entropy methods experimentation

•	**Clustering beasd method ** After the generation and clustering are achieved,  this baseline hallucination detection mechanism will introduce a number of cluster count thresholds, when the number of clusters exceeded the predefined threshold, the model was classified as uncertain, indicating potential hallucinations. We will be experimenting with different thresholds to decide on a suitable one that achieves the best results. 

•	**Semantic entropy method:** After clustering generated responses into semantically distinct groups, we will quantify the distribution of meanings to assess model uncertainty. We will employ Monte Carlo integration to estimate semantic entropy. This approach will sample meaning clusters from the model's output and use them to approximate the true entropy of the meaning distribution. Providing a probabilistic approach to detecting semantic inconsistencies and hallucinations in Arabic LLMs, moving beyond simple threshold-based assessments.


