# UAE Law Model

This repository contains a machine learning model built for legal text analysis, specifically focusing on UAE laws. The model is designed to understand and process legal documents, and can be used for tasks such as legal document classification, question-answering, and information retrieval. The project includes fine-tuning a language model to suit the legal domain using UAE-specific law datasets.

## Overview

The main goal of this project is to develop a machine learning model that can assist in understanding and processing legal texts from UAE laws. The model is built using transformer-based architectures and has been fine-tuned on a dataset of UAE legal documents. This model can be used to assist legal professionals and researchers in extracting meaningful insights and answers from legal texts.

### Key Features:
- **Fine-tuned Transformer Model:** A pre-trained language model (TinyLlama-1b) is fine-tuned on UAE legal texts.
- **PEFT:** The model is quantized to 4-bit and using LoRA to train only about 28% of the model to reduce computational cost
- **Legal Document Analysis:** The model is trained to handle large and complex legal documents, providing insights and answering queries.
- **Customizable for Specific Law Categories:** The model can be adapted to analyze different types of laws (e.g., commercial, criminal, civil).

## Dataset Preparation

Extracting text from several Government issued documents available on UAE gov and performing Data cleaning.
- **Data Type**: The data consisted of english and arabic data, mostly text.
- **Cleaning**: Performed deduplication, splitting to chunks and removal of foreign languages.
- **Evaluation**: Tokenizing the data and evaluating number of tokens procured.

## Dataset

The dataset used for training contains UAE legal documents across different legal domains. It is preprocessed and cleaned to ensure that the model can effectively learn from the data. The dataset includes fields such as:
- **Law kind**: The type of law (e.g., civil, criminal, commercial).
- **Law date & authority**: The date and issuing authority of the law.
- **Content**: The text of the legal document.

## Model

The model is a pretrained TInyLlama-1b model that has been continued pretrained along with finetuning and is trained specifically on legal data. It is capable of performing tasks such as:
- Legal text classification.
- Extracting key information from documents.
- Answering legal questions based on UAE laws.

## Requirements

To run this project, you will need the following Python packages:

-transformers==4.30.2 
-torch==2.0.1 
-pandas==2.1.1 
-numpy==1.23.5 
-scikit-learn==1.3.0

Install the required dependencies using:

```bash
pip install -r requirements.txt
