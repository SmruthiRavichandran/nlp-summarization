
# NLP Summarization

## Overview

This repository provides a robust framework for **text summarization** using Natural Language Processing (NLP) techniques. The project implements multiple summarization algorithms (both extractive and abstractive) with a focus on accuracy, scalability, and ease of use.

## Features

- **Extractive Summarization:** Selects key sentences from the input text to form a coherent summary.
- **Abstractive Summarization:** Generates a summary by rephrasing and paraphrasing the input text.
- Pre-trained models for summarization tasks.
- Support for custom datasets.
- Modular design for easy integration and extension.
- Evaluation metrics like BLEU and ROUGE to assess summarization quality.

---

## Table of Contents

1. [Installation](#installation)
2. [Usage](#usage)
3. [Examples](#examples)
4. [Supported Algorithms](#supported-algorithms)
5. [Datasets](#datasets)
6. [Evaluation](#evaluation)
7. [Contributing](#contributing)
8. [License](#license)

---

## Installation

### Prerequisites

- Python 3.8+
- pip
- Git

### Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/SmruthiRavichandran/nlp-summarization.git
   cd nlp-summarization
   ```

2. Create a virtual environment and activate it:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Verify installation by running the test script:

   ```bash
   python test.py
   ```

---

## Usage

### Quick Start

To summarize text using a pre-trained model:

```bash
python summarize.py --input "Your input text here." --model "abstractive" --output "output_summary.txt"
```

### Command-line Arguments

- `--input`: The input text file or string to summarize.
- `--model`: Model type (`extractive` or `abstractive`).
- `--output`: File path to save the summary.

### Using as a Library

You can also use this repository as a Python module:

```python
from summarizer import Summarizer

# Initialize model
model = Summarizer(model_type="abstractive")

# Summarize text
text = "Your input text here."
summary = model.summarize(text)
print(summary)
```

---

## Examples

### Extractive Summarization

```bash
python summarize.py --input "input.txt" --model "extractive" --output "summary.txt"
```

### Abstractive Summarization

```bash
python summarize.py --input "input.txt" --model "abstractive" --output "summary.txt"
```

### Custom Dataset

To summarize a custom dataset, provide the dataset path:

```bash
python batch_summarize.py --dataset "data/dataset.csv" --model "extractive" --output_dir "summaries/"
```

---

## Supported Algorithms

### Extractive Methods

1. **TextRank:** Graph-based ranking algorithm for key sentence extraction.
2. **TF-IDF:** Statistical approach based on term frequency.

### Abstractive Methods

1. **Seq2Seq:** Encoder-decoder architecture.
2. **Transformer-based Models:** Pre-trained models like BERT and GPT.

---

## Datasets

The following datasets are supported out-of-the-box:

1. **CNN/DailyMail Dataset**
2. **Gigaword**
3. **Custom CSV/JSON datasets**

## Evaluation

The framework supports the following metrics for evaluation:

- **ROUGE (Recall-Oriented Understudy for Gisting Evaluation):** Measures overlap between the generated summary and reference summaries.
- **BLEU (Bilingual Evaluation Understudy):** Evaluates the quality of machine-generated text.

### Example Evaluation Command

```bash
python evaluate.py --generated "output_summary.txt" --reference "reference_summary.txt"
```

---

## Contributing

Contributions are welcome! If you would like to contribute:

1. Fork the repository.
2. Create a feature branch:

   ```bash
   git checkout -b feature-name
   ```

3. Commit your changes and push:

   ```bash
   git commit -m "Feature description"
   git push origin feature-name
   ```

4. Create a pull request.

Please follow the [Contributing Guidelines](CONTRIBUTING.md) for more details.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

