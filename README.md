# stats-ai_ml-term_project
# Speaker Segmentation using Hidden Markov Models (HMM)

## Overview

This repository contains code for segmenting audio recordings into regions corresponding to different speakers, utilizing Hidden Markov Models (HMM). The models are trained on a dataset comprising audio samples from students and professors.

## Getting Started

### Prerequisites

- Python 3
- Required libraries: `glob`, `librosa`, `IPython`, `matplotlib`, `numpy`, `scikit-learn`, `hmmlearn`

bash
pip install glob2 librosa ipython matplotlib numpy scikit-learn hmmlearn


### Dataset

The audio dataset should be organized into `./dataset/train` and `./dataset/valid` directories for training and validation, respectively. The dataset contains classes 'student' and 'professor'.

## Usage

1. *Data Preparation*

   - Load file paths and audio classes for training and validation.
   - Reshape audio files into segments.

2. *Feature Extraction*

   - Extract features such as chroma, RMS, spectral centroid, spectral bandwidth, spectral rolloff, zero-crossing rate, and MFCC from audio segments.

3. *Data Scaling*

   - Standardize features using `StandardScaler` from scikit-learn.

4. *Model Training and Evaluation*

   - Train HMM models with different parameters (`n_components`, `n_iter`) for each speaker class.
   - Evaluate the models on the validation set.

5. *Segmentation of New Audio File*

   - Load and reshape a new audio file.
   - Extract features and scale them.
   - Use trained models to predict speaker segments.

6. *Results*

   - Display and listen to the segmented audio for each speaker class.

## Model Parameters

Experiment with different HMM parameters (`n_components`, `n_iter`) to optimize performance on your dataset.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- This project uses the HMM implementation from the [hmmlearn](https://hmmlearn.readthedocs.io/en/stable/) library.

Feel free to contribute or report issues!
