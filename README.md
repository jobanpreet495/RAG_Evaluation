# Retrieval-Augmented Generation (RAG) Evaluation

This repository provides an overview and evaluation framework for **Retrieval-Augmented Generation (RAG)** systems, which enhance the capabilities of Large Language Models (LLMs) by incorporating external knowledge during response generation.

## Overview

RAG addresses the following challenges in LLMs:
- **Knowledge limitations**: Overcomes the static nature of LLM training data by incorporating real-time, domain-specific context.
- **Context window limitations**: Efficiently includes relevant information without exceeding context length.
- **Hallucinations**: Mitigates incorrect or fabricated responses by grounding outputs in retrieved evidence.

### Key Components of RAG
1. **Retriever**: Retrieves relevant context from external databases or knowledge sources.
2. **Generator**: Produces responses by combining the retrieved context with the user query.

### Why Evaluate RAG?
For robust performance, it is crucial to evaluate:
- The **Retriever**: Accuracy and relevance of retrieved context.
- The **Generator**: Quality and correctness of the generated responses based on the provided context.

### Retrieval Component
* Context precision - It measures the signal-to-noise ratio of the retrieved context. This metric is computed using the question and the contexts
* Context Recall - This metric states that if all the relevant information required to answer the question was retrieved. This metric is computed based on the ground_truth .

### Generator Component
* Faithfulness - It measures the factual accuracy of the generated answer.The number of correct statements from the given contexts is divided by the total number of statements in the generated answer. This metric uses the question, contextsand the answer.
* Answer relevancy - It measures how relevant the generated answer is to the question. This metric is computed using the question and the answer. For example, the answer “France is in western Europe.” to the question “Where is France and what is it’s capital?” would achieve a low answer relevancy because it only answers half of the question.


### Prerequisites
- Python 3.10 or higher.
- Required Python libraries (specified in the notebook).



