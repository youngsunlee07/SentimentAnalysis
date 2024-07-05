# Sentiment Analysis
This project implements a sentiment analysis model using a bigram language model. The model is trained on the SST-2 dataset and predicts the sentiment of sentences as either positive or negative.

## Components
1. Data Preparation:
- Tokenizes sentences.
- Splits data into training, validation, and test sets.
- Computes prior probabilities of positive and negative sentiments.

2. Bigram Language Model:
- Counts bigrams in tokenized sentences.
- Computes smoothed probabilities for bigrams using additive smoothing.

3. Model Evaluation:
- Computes log probabilities of sentences.
- Selects the best smoothing parameter (alpha) based on log likelihood.
- Evaluates the model on the test set.

## Installation
To run this project, you need to have Python installed. You can install the required packages using pip:
```bash
pip install numpy pandas nltk scikit-learn
```

## Dataset
This project uses the SST-2 dataset. You need to download the dataset from https://gluebenchmark.com/tasks and place it in the following directory structure:

```perl
<project_root>/
│
├── Data/
│   └── SST-2/
│       ├── train.tsv
│       ├── dev.tsv
│       └── test.tsv
│
└── SentimentAnalysis.ipynb
```

## Usage
1. Clone the repository:
```bash
git clone https://github.com/yourusername/SentimentAnalysis.git
cd SentimentAnalysis
```

2. Place the SST-2 dataset in the Data/SST-2/ directory as shown above.

3. Open the 'SentimentAnalysis.ipynb' file and replace 'file path' with the actual file path where the SST-2 dataset is located. For example: 

```bash 
file_path_sst = r'path_to_your_data/Data/SST-2'
full_path = os.path.join(file_path_sst, "train.tsv")
```

4. Run the Jupyter Notebook:
```bash
jupyter notebook SentimentAnalysis.ipynb
``` 

## Contact
If you have any questions or suggestions about the project, please contact me at youngsun.lee07@gmail.com.
