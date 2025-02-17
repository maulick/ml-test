<p align="center">
  <img width="621" alt="logo" src="https://user-images.githubusercontent.com/76659596/105877123-eb112280-5fff-11eb-9425-8432e693f92e.png">
</p>

[![online hosted application](https://img.shields.io/static/v1?label=Try-It-Out&message=Online-Hosted-Application&color=yellow&logo=godot-engine)](https://huggingface.co/spaces/Baishali/Comments-Toxicity-Detection)
[![License - Apache-2.0](https://img.shields.io/badge/License-Apache-blue)](#license)
[![Build - Passing](https://img.shields.io/badge/Build-Passing-brightgreen)](https://github.com/baishalidutta/Comments-Toxicity-Detection/runs/1485969918)
[![GitHub release](https://img.shields.io/github/release/baishalidutta/Comments-Toxicity-Detection?include_prereleases&sort=semver)](https://github.com/baishalidutta/Comments-Toxicity-Detection/releases/)
![Python](https://img.shields.io/badge/python-v3.7.0+-blue.svg)
[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/baishalidutta/Pneumonia-Detection/issues)

<p align="center">
  <img width="721" alt="web-app-screencast" src="https://user-images.githubusercontent.com/76659596/108608735-37663d00-73c9-11eb-8e6e-304dd535f527.gif">
</p>

## Motivation

People tend to discuss or share opinions on social platforms but such activities sometimes encounter threats or harassments which compel people to not express themselves properly.

Many social platforms try to find out such harassments or threats in conversations so that such conversations can easily be prevented before it causes any further damage.

Toxicity detection in comments is one of such methodologies to find out the different types of conversations that can be classified as toxic in nature.

To increase the efficacy in classifying such comments, we can make use of machine learning algorithms to determine the toxicity in comments. 

In this model, many toxic comments have been fed to build a `Bidirectional Long Short-Term Memory (LSTM) Recurrent Neural Network (RNN)` model for fulfilling the purpose.

## Requirements

- Python 3.7.0+
- Tensorflow 2.4.1+
- Keras 2.4.3+
- matplotlib 3.3.3+
- numpy 1.19.5+
- pandas 1.2.1+
- scikit-learn 0.24.1+ 
- nltk 3.5+
- spacy 3.0.3+
- textblob 0.15.3+
- gradio 1.5.3+

## Dataset

You can downloaded the dataset from [kaggle](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge). Use the underlying download link to download the dataset.

### Instructions

* Navigate to `data` section
* In the `Data Explorer`, you will find four separate zip archives to download
* Download `test.csv.zip`, `test_labels.csv.zip` and `train.csv.zip`
* Extract the files
* Copy the CSV files to the `data` directory

The following list enumerates different classes (types) of comments -

| Toxic | Very Toxic | Obscene | Threat | Insult | Hate | Neutral |
|-------|------------|---------|--------|--------|------|---------|


## Installation

* Clone the repository 

`git clone https://github.com/baishalidutta/Comments-Toxicity-Detection.git`

* Install the required libraries

`pip3 install -r requirements.txt`

## Model Ideology

* `Clean text`: 
    * Lower all text
    * Remove uncommon signs
    * Expand abbreviations
    * Correct misspelled words
    * Remove punctuations
    * Remove emojis
    * Remove stop words
    * Apply lemmatisation
* `Tokenize text` data
* Create `Embedding Vector` using [Glove.6B](https://nlp.stanford.edu/projects/glove/)
* Train a `Recurrent Neural Network (RNN)` with a `Bidirectional LSTM` layer

## Usage

Navigate to the `source` directory to execute the following source codes.

* To generate the model on your own, run

`python3 model_training.py`

* You can also provide your own CSV data:

`python3 model_training.py --data=csv_file_location`

* To evaluate any dataset using the pre-trained model (in the `model` directory), run

`python3 model_evaluation.py`

Note that, for evaluation, `model_evaluation.py` will use the `test.csv` and `test_labels.csv` (inside `data` directory).

Alternatively, you can find the whole analysis in the notebook inside the `notebook` directory. To open the notebook, use either `jupyter notebook` or `google colab` or any other IDE that supports notebook feature such as `PyCharm Professional`.

## Web Application

To run the web application locally, go to the `webapp` directory and execute:

`python3 web_app.py`

This will start a local server that you can access in your browser. You can type in any comment and find out what toxicity the model determines.

You can, alternatively, try out the hosted web application [here](https://gradio.app/g/baishalidutta/Comments-Toxicity-Detection).

## Developer

Baishali Dutta (<a href='mailto:me@itsbaishali.com'>me@itsbaishali.com</a>)

## Contribution [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/baishalidutta/Comments-Toxicity-Detection/issues)

If you would like to contribute and improve the model further, check out the [Contribution Guide](https://github.com/baishalidutta/Comments-Toxicity-Detection/blob/main/CONTRIBUTING.md)

## License [![License](http://img.shields.io/badge/license-Apache-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)

This project is licensed under Apache License Version 2.0
