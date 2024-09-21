### README.md

# PromptGenCLI

This repository demonstrates how to interact with OpenAI's API to generate text-based responses using customizable inference parameters. The program allows developers to send a prompt to a selected model, returning a detailed response based on specific input parameters like temperature and top-p, which influence the response variability and output length.

## Features

- **Model Customization**: Choose from different OpenAI models to generate text-based completions.
- **Inference Parameters**: Control the variability of the response using temperature and top-p, which adjust how creative or focused the model should be.
- **Token Length**: Supports up to 2000 tokens per response, controlling the length and complexity of generated text.
- **Command-Line Interface**: Accepts input model and prompt through command-line arguments for flexible usage.
- **Stop Sequences**: Optional inference parameters (like Stop Sequences) can be used to fine-tune when and how the response should end, preventing unwanted or repetitive outputs.

## Inference Parameters Overview

Inference parameters customize how the foundation model behaves. These include:

- **Temperature**: Controls the randomness of the model’s output. A higher temperature (e.g., 1.0) makes the output more diverse, while a lower value (e.g., 0) makes it more deterministic.
  
- **Top-p**: Adjusts how much of the output is focused on the highest probability tokens. Lower top-p values restrict the output to more likely tokens.

- **Max Tokens**: Determines the maximum length of the output, where tokens can be either a word or part of a word.

- **Stop Sequences**: Help in controlling the end of the response, stopping the output when a certain phrase or token sequence is encountered.

## Usage

### Prerequisites

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/PromptGenCLI.git
   ```

2. Install dependencies:
   ```bash
   pip install openai python-dotenv
   ```

3. Create a `.env` file and add your OpenAI API key:
   ```env
   OPENAI_API_KEY=your-api-key-here
   ```

### Running the Program

The program accepts two arguments:
1. The OpenAI model (e.g., `gpt-3.5-turbo`)
2. The prompt for the model to process.

To run the program:
```bash
python app.py gpt-3.5-turbo "What is the meaning of life?"
```

### Example Output
```
The meaning of life can vary greatly depending on personal beliefs, culture, and experiences...
```

## Customization

Modify the `temperature`, `top_p`, or `max_tokens` to change the behavior and length of responses:
- `temperature`: Set between 0 and 1 for more varied or focused responses.
- `top_p`: Set between 0 and 1 to adjust the probability distribution of token selection.
  
## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
