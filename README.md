# Harry Potter Chatbot

## Project Description

This project offers Harry Potter fans a unique opportunity to interact with a witty and entertaining AI, designed to emulate the personas of the beloved characters from the Harry Potter universe.

### **Approach**

1. **Data Pre-processing**:
    - Conversations are extracted and pre-processed based on characters, starting with Harry as the primary focus.
    - This modular framework allows for easy extension, enabling the addition of other characters such as Hermione and Ron.
    
2. **Harry Potter Dataset**:
    - A curated dataset includes dialogues and interactions from the Harry Potter series.
    - Dialogues are modified with a humorous twist, ensuring responses are both contextually relevant and entertaining.

3. **Pre-trained DialoGPT Model**:
    - Utilizes Microsoft's [DialoGPT](https://huggingface.co/microsoft/DialoGPT-large), a state-of-the-art conversational AI model.
    - Known for generating human-like responses, DialoGPT serves as the foundation of our chatbot.

4. **Fine-tuning**:
    - The DialoGPT model is fine-tuned on the Harry Potter dataset for three epochs.
    - This allows the model to adapt to the unique language, tone, and humor of the Harry Potter universe.

5. **Character-based Conversations**:
    - Enables users to interact with different characters from the Harry Potter series.
    - This feature provides an immersive and personalized chatbot experience.

---

## Features
- **Interactive Conversations**: Chat with AI personalities modeled after Harry Potter characters.
- **Extensible Framework**: Add new characters like Hermione or Ron with minimal effort.
- **Humorous and Contextually Relevant Responses**: Ensure user engagement through entertaining and meaningful interactions.

---

## Installation

### **Requirements**
- Python 3.8+
- PyTorch
- Hugging Face Transformers
- NVIDIA Apex (optional, for mixed-precision training)

## Parameters

### **Training**
- `--train_batch_size`: Number of samples per batch during training. *(Default: 8)*
- `--learning_rate`: Initial learning rate for the optimizer. *(Default: 5e-5)*
- `--gradient_accumulation_steps`: Number of steps to accumulate gradients before performing an optimizer step. *(Default: 1)*
- `--num_train_epochs`: Total number of training epochs. *(Default: 3)*
- `--warmup_steps`: Number of steps for learning rate warm-up. *(Default: 500)*

### **Evaluation**
- `--eval_batch_size`: Number of samples per batch during evaluation. *(Default: 8)*
- `--evaluation_strategy`: Evaluation strategy during training (e.g., "steps" or "epoch"). *(Default: "epoch")*
- `--logging_steps`: Frequency (in steps) for logging metrics. *(Default: 500)*

### **Interaction**
- `--max_length`: Maximum token length for generated responses. *(Default: 200)*
- `--top_k`: Filters to the top-k most probable tokens at each decoding step for response diversity. *(Default: 50)*
- `--top_p`: Probability threshold for nucleus sampling to control diversity. *(Default: 0.9)*
- `--temperature`: Sampling temperature; higher values generate more random responses. *(Default: 0.7)*

### **Additional Optional Parameters**
- `--fp16`: Enable mixed-precision training for faster performance. *(Default: False)*
- `--save_steps`: Frequency (in steps) to save checkpoints during training. *(Default: 1000)*


Use this configuration set to tailor the training, evaluation, and interaction phases of the chatbot to your specific requirements.

