# Arabic Text Summarization using AraT5

This notebook demonstrates how to fine-tune the [AraT5](https://huggingface.co/UBC-NLP/AraT5v2-base-1024) model on the [XLSum](https://huggingface.co/datasets/csebuetnlp/xlsum) dataset to perform Arabic text summarization.

## Model and Dataset
- Model: AraT5, a pre-trained T5 model tailored for Arabic natural language processing tasks.
- Dataset: XLSum, a dataset consisting of diverse multilingual summaries, specifically fine-tuned for Arabic text summarization.

## Task
The goal of this task is to generate concise, meaningful summaries for long Arabic text using a transformer-based model. The model is fine-tuned on the XLSum dataset to learn how to summarize content effectively.

## Training
- Preprocessing: The XLSum dataset is tokenized and preprocessed to fit the input format required by the T5 model.
- Evaluation : using the [ROUGE](https://pypi.org/project/rouge-score/) to evalute the Arabic generated summaries which allow us to choose a specific `tokenizer`
- Baseline accuracy : apply the `lead-3 baseline` to get strong baseline performance
- Fine-tuning: AraT5 is fine-tuned on the Arabic subset of XLSum. The model is trained using techniques such as learning rate scheduling and model checkpointing to optimize 
performance.

## Usage
To use this notebook, simply clone the repository and run the cells. The fine-tuned model can generate Arabic text summaries from longer input texts.
