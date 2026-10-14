# Moroccan Darija Text-to-Speech with SpeechT5

Fine-tuning Microsoft's SpeechT5 model for Text-to-Speech (TTS) experimentation in Moroccan Darija using audio-text data stored in Parquet files.

## Overview

This project explores adapting a pretrained speech synthesis model to Moroccan Darija. It covers dataset preparation, text normalization, audio preprocessing, speaker embedding extraction, model fine-tuning, and speech generation.

## Features

- Load and merge multi-part Parquet datasets
- Normalize Darija text and experiment with Arabizi conversion
- Preprocess audio for model training
- Extract speaker embeddings using SpeechBrain
- Fine-tune SpeechT5 with Hugging Face Transformers
- Generate speech and inspect audio characteristics

## Tech Stack

- Python and PyTorch
- Hugging Face Transformers and Datasets
- SpeechBrain
- Librosa and SoundFile
- Pandas, NumPy and PyArrow
- Google Colab

## Models

- **TTS model:** [microsoft/speecht5_tts](https://huggingface.co/microsoft/speecht5_tts)
- **Vocoder:** [microsoft/speecht5_hifigan](https://huggingface.co/microsoft/speecht5_hifigan)
- **Speaker embeddings:** SpeechBrain x-vector model

## Project Workflow

1. Load and inspect the audio-text dataset.
2. Normalize Darija text and preprocess audio.
3. Extract speaker embeddings.
4. Prepare the training data.
5. Fine-tune SpeechT5.
6. Evaluate the experiment and generate speech samples.

## Dataset

The project uses Parquet files containing audio samples and their corresponding Darija text.

The dataset is not included in this repository. Users must obtain the data from an authorized source and verify its license and redistribution conditions.

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/fatiassouli/moroccan-darija-tts.git
cd moroccan-darija-tts
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

A compatible Python environment is required. Google Colab with GPU support is recommended for practical fine-tuning.

### 3. Prepare the dataset

Mount Google Drive in Colab and update the notebook paths to point to your authorized Parquet files.

### 4. Run the notebook

Open `Code_TTS.ipynb` in Google Colab and execute the notebook sections in order.

## Recorded Experiment

The original notebook contains a recorded training run of 4,000 steps and an evaluation loss of approximately 0.4536.

This records an experiment; the loss alone does not establish pronunciation accuracy or perceived speech quality.

## Limitations

- Arabizi-to-Arabic conversion requires further validation.
- Audio signal statistics alone cannot establish perceived speech quality.
- The notebook depends on external dataset files and environment-specific paths.
- Reproducing the experiment requires compatible dependencies and sufficient computing resources.

## Future Improvements

- Improve Darija text normalization.
- Validate preprocessing on diverse Darija examples.
- Document a reproducible training configuration.
- Add qualitative and quantitative evaluation.
- Publish audio examples when redistribution is permitted.

## Author

**Fatima Zahraa Assouli**

AI and Deep Learning student

[GitHub Profile](https://github.com/fatiassouli)

## Acknowledgements

This project builds on the work and tools provided by the SpeechT5 authors, Hugging Face, and SpeechBrain.