# GPT Language Model | PyTorch

## Project Overview

A character-level GPT model built from scratch in PyTorch, featuring multi-head self-attention and Transformer blocks for text generation. Trained on a text corpus with configurable hyperparameters for flexible experimentation, this project demonstrates language modeling and generative capabilities.

## Key Features

- **Character-level GPT model:** Built using PyTorch with a focus on multi-head self-attention and Transformer architecture.
- **Text generation:** Trained on text data and capable of generating human-like text sequences.
- **Configurable hyperparameters:** Offers flexibility for adjusting parameters like batch size, block size, number of layers, and attention heads.
- **Training pipeline:** Custom model training and evaluation routines to monitor progress and loss.

## Technologies Used

- **PyTorch** for deep learning and model development.
- **Transformer architecture** for self-attention and sequence modeling.
- **Python** for scripting and data processing.
- **Natural Language Processing (NLP)** for text data handling.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/GPT-Language-Model.git
   cd GPT

2. Generating Text :
   ```bash
   context = torch.zeros((1, 1), dtype=torch.long, device=device)
   print(decode(m.generate(context, max_new_tokens=500)[0].tolist()))
  The text generated will be based on the learned patterns from the training dataset.

## Model Architecture
This model uses a series of modular blocks that align with GPT architecture principles:

- Self-Attention Layer: Computes relationships between tokens within the context window.
- Multi-Head Attention: Allows the model to focus on different parts of the sequence simultaneously.
- Feed-Forward Network: Processes the aggregated information and applies transformations.
- Layer Normalization and Dropout: Enhances model stability and regularization.
- The model contains:

    - 6 Transformer blocks.
    - 6 self-attention heads per block.
    - An embedding size of 384.
    - Over 10 million parameters.
    - This design is aimed at capturing complex relationships in text.
 
## Hyperparameters
Adjustable hyperparameters are defined at the beginning of the code, allowing easy tuning for custom applications:

| Hyperparameters | Description     | Default               |
| :-------- | :------- | :------------------------- |
| `batch_size` | Number of sequences processed in parallel | 64 |
| `block_size` | Maximum context length for predictions   | 256              |
| `learning_rate` | Learning rate for optimization | 3e-4 |
| `n_embd` | Embedding size for tokens   | 384               |
| `n_head` | Number of attention heads per layer | 6|
| `n_layer` | Number of Transformer blocks   | 6             |
| `dropout` | Dropout rate for regularization |0.2|


