# Log Classification NLP

A toolkit for classifying log messages using NLP, regex, and large language models. Designed for automation, monitoring, and analytics in log-heavy environments.

---

## Features

- **Traditional ML Classification:** Uses scikit-learn for classic log classification.
- **BERT Embeddings:** Leverages sentence-transformers for semantic log understanding.
- **Regex-based Classification:** Fast, rule-based log categorization.
- **LLM Integration:** Supports Groq API for advanced log analysis.
- **Configurable Pipelines:** Easily switch between classification methods.
- **Environment Variable Support:** Uses `.env` for API keys and config.

---

## Getting Started

### 1. Clone the Repository

```sh
git clone https://github.com/yourusername/log_classification_nlp.git
cd log_classification_nlp
```

### 2. Install Dependencies

```sh
pip install -r requirements.txt
```

### 3. Environment Setup

Create a `.env` file in the root directory for sensitive configs (e.g., API keys):

```
GROQ_API_KEY=your_groq_api_key
MODEL_PATH=models/your_model.pkl
```

---

## Usage

### Log Classification

Run the main script to classify logs:

```sh
python classify.py --input resources/logs.csv --output resources/classified_logs.csv --method bert
```

- `--input`: Path to input CSV file with logs.
- `--output`: Path to save classified logs.
- `--method`: Classification method (`ml`, `bert`, `regex`, `llm`).

### Training

Train a new model using the provided notebook:

```sh
jupyter notebook training/training.ipynb
```

---

## File Structure

```
├── classify.py
├── processor_bert.py
├── processor_llm.py
├── processor_regex.py
├── models/
│   └── *.pkl
├── resources/
│   ├── logs.csv
│   └── classified_logs.csv
├── training/
│   └── training.ipynb
├── requirements.txt
├── .env
└── README.md
```

---

## API Integration

- **Groq API:** Used for LLM-based classification. Requires API key in `.env`.

---

## Contributing

1. Fork the repo.
2. Create a feature branch.
3. Submit a pull request.

---

## License

MIT License

---

## Contact

For questions or support, open an issue or