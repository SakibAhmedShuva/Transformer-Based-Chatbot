# Transformer-Based-Chatbot

A simple question-answering chatbot implementation using Hugging Face's Transformers library and DistilBERT model.

## Overview

This project demonstrates the implementation of a question-answering system using transformer-based models. The chatbot can understand context and answer questions based on provided text passages.

## Features

- Question-answering capabilities using DistilBERT model
- Context-aware responses
- Easy-to-use implementation
- Built on Hugging Face's Transformers library

## Requirements

- Python 3.7+
- transformers
- torch
- numpy

## Installation

```bash
pip install transformers torch numpy
```

## Usage

The main implementation is in the `chatbot_tf.ipynb` notebook. To use the chatbot:

1. Import the required libraries
2. Load the question-answering pipeline
3. Provide context text
4. Ask questions about the context

Example:

```python
from transformers import pipeline

# Initialize the pipeline
pipe = pipeline('question-answering', model="distilbert/distilbert-base-cased-distilled-squad")

# Provide context
text = """Your context text here"""

# Ask questions
question = "Your question here"
result = pipe(question=question, context=text)
```

## Model Details

- Model: DistilBERT (distilbert-base-cased-distilled-squad)
- Task: Question Answering
- Framework: Hugging Face Transformers

## Example Output

```python
# Question: "How many cats did Rambo have?"
# Answer: "9"

# Question: "How many cats were male?"
# Answer: "2"
```

## Limitations

- Requires explicit context for each question
- Answers are extracted directly from the provided text
- Performance depends on the quality and relevance of the context

## Contributing

Feel free to open issues or submit pull requests for improvements.

## License

MIT License

## Acknowledgments

- Hugging Face for the Transformers library
- DistilBERT model creators
