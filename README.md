# Advanced Question Answering System

This repository contains an advanced question-answering system that utilizes OpenAI's language models, FAISS for efficient similarity search, and document handling capabilities to perform detailed text analysis and generate contextually relevant questions and answers.

## Features

- **Question Generation**: Leverages OpenAI's GPT-3.5 model to generate relevant questions from textual content.
- **Question Retreival**: Retreive the hypothetical questions which are most relevant to the user's input query.
- **Document Retrieval**: Utilizes FAISS (Facebook AI Similarity Search) to efficiently retrieve documents related to user queries.
- **Answer Generation**: Retreived the relevant context to each question, check if any chunk appear more than once and dicsard repeated chunks. Generate the answer using the relevant context of all hypothetical questions.
- **Context and Answer Evaluation**: This code will enable you to analyse that your retreived chunk is relavant to the user question or not. It also compares multiple answers to determine which is most relevant or correct using a structured grading system.
- **Document Formatting**: Outputs analysis and results into well-structured `.docx` files for easy dissemination and review.

## Installation

Ensure you have Python 3.8+ installed, then clone this repository and install the required packages:

```bash
git clone https://github.com/your-username/advanced-qa-system.git
cd advanced-qa-system
pip install -r requirements.txt
```

# Usage
**Setting Up**
First, set your API keys for OpenAI and any other services in your environment variables or pass them directly into the script.

**Running the Scripts**
Navigate to the project directory and run the Jupyter Notebook or Python scripts.

**Generating Questions**
Use the provided functionality to generate questions based on your documents:
```bash
questions = generate_questions(text_chunk, num_questions=5, API_KEY='Your-OpenAI-API-Key')
```
Evaluating Answers
Compare and evaluate two given answers to determine which is more relevant or accurate:


```bash
evaluation = answer_evaluator.invoke({
    "context": document_content,
    "question": "What is the inheritance pattern of Duchenne Muscular Dystrophy?",
    "answer1": "It is an autosomal recessive disorder.",
    "answer2": "It is inherited through an X-linked recessive pattern."
})
```
