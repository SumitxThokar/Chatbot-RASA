# Rock-Paper-Scissors Chatbot using Rasa


## Overview

This repository contains the code for a chatbot that plays the classic game "Rock, Paper, Scissors" using Rasa, an open-source conversational AI framework. The chatbot allows users to interact with it through a chat interface and play multiple rounds of the game against the bot.

## Prerequisites

Before running the chatbot, ensure you have the following installed:

1. Python (>=3.6)
2. Rasa (>=2.0)

## Installation

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/your-username/rock-paper-scissors-chatbot.git
   cd rock-paper-scissors-chatbot
   ```

2. Create a virtual environment (optional but recommended):

   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows, use "venv\Scripts\activate"
   ```

3. Install the required Python packages:

   ```bash
   pip install -r requirements.txt
   ```

## Training the Chatbot

To train the chatbot, execute the following command:

```bash
rasa train
```

This command will take care of training the NLU (Natural Language Understanding) and Core (Dialogue Management) models using the provided training data and configuration.

## Running the Chatbot

To run the chatbot, use the following command:

```bash
rasa run actions &
rasa run -m models --enable-api --cors "*" --debug
```

The first command starts the custom actions server, and the second command runs the Rasa chatbot with the trained models. The `--enable-api` flag allows the chatbot to communicate with the custom actions server.

## Interacting with the Chatbot

Once the chatbot is up and running, you can interact with it through a REST API or the Rasa interactive shell. To use the interactive shell, execute the following command:

```bash
rasa shell
```

The chatbot will greet you and provide instructions on how to play Rock, Paper, Scissors. You can type your choice (rock, paper, or scissors), and the chatbot will respond with its choice and the result of the round.

## Customization

If you wish to customize the chatbot's responses, actions, or training data, you can modify the corresponding files in the `data/` and `actions/` directories. For example, to change the chatbot's responses, edit the `responses.yml` file.


Happy coding! 🎉
