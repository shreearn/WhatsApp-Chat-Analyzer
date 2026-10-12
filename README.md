# WhatsApp Chat Analyzer

Upload any exported WhatsApp chat and get an instant, interactive breakdown of who talks most, when the group is active, what people talk about, and the overall mood of the conversation.

![Python 3.x](https://img.shields.io/badge/Python-3.x-blue)
![Streamlit App](https://img.shields.io/badge/Streamlit-App-ff4b4b)
![NLP NLTK VADER](https://img.shields.io/badge/NLP-NLTK%20VADER-green)
![Python 3.x](https://img.shields.io/badge/Python-3.x-blue)
![Plotly Interactive Charts](https://img.shields.io/badge/Plotly-Interactive%20Charts-3f4f75)

[🔗 Try the live app](https://whatsapp-chat-analyzer-asxkkmsg7tccppetijqnfq.streamlit.app/)

# What It Does

Group chats contain thousands of unstructured messages full of slang, emojis, links and mixed languages. This app turns that raw text into a clean analytics dashboard, for the whole group or for any individual participant.


# Features

Area	| Insights

📊 Top Statistics:	Total messages, words, media shared and links shared

📅 Timelines:	Monthly and daily message activity

🔥 Activity Maps:	Busiest days and months, plus a weekday × hour activity heatmap

👥 User Analysis:	Most active members and their share of the conversation

☁️ Text Analysis:	Word cloud and most common words

😀 Emoji Analysis:	Most-used emojis and their distribution

💬 Sentiment Analysis:	Positive, neutral and negative tone using NLTK VADER

🦉 Fun Facts:	The group's night owls and early birds


# How It Works

Exported chat (.txt)
  
   │
   
   ├─ Parsing ........... regex extracts timestamp, sender and message from each line
   
   ├─ Cleaning .......... removes links, media placeholders, punctuation and numbers
   
   ├─ Stop words ........ custom English + Hinglish + Marathi lists for mixed-language chats
   
   ├─ Feature building .. date, day, month and hour features for time-based analysis
   
   └─ Analysis .......... stats, word frequency, emoji counts, VADER sentiment

Handling mixed-language chats: Indian group chats often switch between English, Hindi (written in English letters) and Marathi. Standard English stop-word lists miss most filler words in these chats, so custom stop-word lists were added to make word clouds and frequency analysis meaningful.

To export a chat: open a WhatsApp chat → ⋮ → More → Export chat → Without media. Upload the .txt file in the sidebar.

No chat handy? Download the built-in sample chat from the sidebar. It's a synthetic conversation created for demo purposes.

# project Structure

├── app.py              # Streamlit UI and layout

├── preprocessor.py     # chat parsing into a structured DataFrame

├── helper.py           # statistics, text cleaning, emoji and sentiment analysis

├── stop_hinglish.txt   # custom stop-word list

├── styles/main.css     # custom styling

├── test.txt            # synthetic sample chat

└── requirements.txt

# Privacy

Uploaded chats are processed in memory during the session and are not stored.

# Tech Stack

Language & Data: Python, Pandas, NumPy, Regex 

NLP: NLTK (VADER sentiment), WordCloud, emoji, URLExtract 

Visualization: Matplotlib, Seaborn, Plotly, ECharts App: Streamlit
