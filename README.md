# MiloBot – A Generative Seq2Seq Chatbot in PyTorch

MiloBot is a simple generative chatbot built using a sequence-to-sequence (Seq2Seq) architecture with PyTorch. Developed as part of an academic mini-project, it allows you to train and test a conversational AI model on your own chat data. The project includes a full pipeline for preprocessing, training, and evaluation.

## Getting Started

To use your own data, prepare a `.tsv` or `.csv` with your data. Then run the preprocessing script:

```bash
jupyter preprocess_chat.ipynb --data_path path/to/your_chat_data.tsv
```

This will create a file called `organised_chat.tsv` to be used for training.

To train the chatbot, open and run:

```bash
jupyter notebook seq2seq_milobot_train.ipynb
```

Checkpoints will be saved to `ckpt/chatbot/` every 500 iterations.

Once training is complete, you can interact with the chatbot via the terminal using:

```bash
python seq2seq_chatbot_test.py --ckpt ckpt/chatbot/500_checkpoint.pt
```

Replace `500` with your desired checkpoint number. On Windows, run this in the Anaconda Prompt and ensure your environment is activated.

## Requirements

Install dependencies with:

```bash
pip install -r requirements.txt
```

Using a virtual environment is recommended.

## Notes

This project is intended as a proof of concept. MiloBot was trained on a small dataset (~2000 messages), and performance is limited accordingly.

The training notebook is adapted from course materials provided as part of an NLP module. Model architecture was provided by instructors; this version includes modifications in data handling, training configuration, and evaluation.

## Acknowledgments

Adapted and extended by Ina Hrešć. Core model structure developed as part of university coursework.