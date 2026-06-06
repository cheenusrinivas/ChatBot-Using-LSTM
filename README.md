# 🤖 Chatbot using Seq2Seq LSTM Models

A conversational AI chatbot built using Sequence-to-Sequence 
(Seq2Seq) LSTM neural networks. The model learns to understand 
questions and generate human-like responses by training on 
real conversation datasets.

---

## 🧠 What is Seq2Seq?

Sequence-to-Sequence is a deep learning architecture where:
- An **Encoder** reads the input question and compresses 
  it into a context vector (LSTM states h and c)
- A **Decoder** takes that context and generates 
  the response word by word

Think of it like Google Translate — but for conversations!

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core programming language |
| TensorFlow / Keras | Building and training the LSTM model |
| NumPy | Numerical operations and array handling |
| YAML | Parsing the conversation dataset files |
| Gensim (Word2Vec) | Word tokenization and vocabulary building |
| Google Colab | Training environment with GPU support |
| Kaggle API | Downloading the chatbot dataset |
| TFLite | Converting model for edge device deployment |

---

## 🏗️ How It Works

### Architecture

Input Question
↓
Embedding Layer (200 dimensions)
↓
LSTM Encoder → produces state_h, state_c
↓
LSTM Decoder (initialized with encoder states)
↓
Dense Layer (Softmax activation)
↓
Predicted Answer Word by Word

### Steps
1. **Data Collection** — Downloaded ChatterBot English 
   dataset from Kaggle with thousands of Q&A pairs
2. **Preprocessing** — Tokenized text, added START/END 
   tokens, padded sequences
3. **Training** — 150 epochs, RMSprop optimizer, 
   Categorical Crossentropy loss
4. **Inference** — Encoder encodes question, decoder 
   generates answer word by word
5. **TFLite** — Converted model for mobile deployment

---

## 💬 Example

Enter question: What is your name?

I am a chatbot built using deep learning.

Enter question: How are you?

I am doing well thank you for asking.


---

## 🚀 How to Run

1. Open notebook in **Google Colab**
2. Upload your `kaggle.json` API key when prompted
3. Run all cells in order
4. Chat with the bot in the final cell

> ⚠️ Recommended to run in Google Colab — 
> requires GPU for training

---

## 📚 What I Learned

- Seq2Seq architecture for NLP tasks
- Text preprocessing — tokenization, padding, 
  one-hot encoding
- Building and training LSTM models with TensorFlow/Keras
- Encoder-Decoder inference for text generation
- Converting deep learning models to TFLite

---

## 👨‍💻 Author

**Srinivas Udhayasankar**
- 🌐 [Portfolio](https://srinivasudhayasankarportfolio.netlify.app)
- 💼 [LinkedIn](https://linkedin.com/in/srinivas-udhayasankar)
- 🐙 [GitHub](https://github.com/cheenusrinivas)

Then push:
bashgit add .
git commit -m "added README"
git push
