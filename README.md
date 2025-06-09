# AI-Mental-Health-Companion
import streamlit as st
import random

st.set_page_config(page_title="AI Mental Health Companion", page_icon="🧠", layout="centered")

# ---- Title ----
st.title("🧠 AI Emotional Support & Wellness Companion")
st.write("Feeling low, anxious, or just need a boost? Let this AI buddy guide your emotions and uplift your spirit!")

# ---- Emotion Input ----
emotion = st.selectbox(
    "How are you feeling right now?",
    ["happy", "sad", "angry", "anxious", "tired", "stressed"]
)

# ---- Motivational Quotes ----
quotes = {
    "happy": [
        "Happiness is a direction, not a place. – Sydney J. Harris",
        "Enjoy the little things in life. – Robert Brault"
    ],
    "sad": [
        "Even the darkest night will end and the sun will rise. – Victor Hugo",
        "Tough times never last, but tough people do. – Robert H. Schuller"
    ],
    "angry": [
        "Speak when you are angry and you’ll make the best speech you’ll ever regret. – Ambrose Bierce",
        "Let your anger be like a monkey in a box—contained and funny."
    ],
    "anxious": [
        "Anxiety does not empty tomorrow of its sorrows. – Charles Spurgeon",
        "You don’t have to control your thoughts. Just stop letting them control you. – Dan Millman"
    ],
    "tired": [
        "Rest when you’re weary. Refresh and renew yourself. – Naomi Judd",
        "Sometimes the most productive thing you can do is rest. – Mark Black"
    ],
    "stressed": [
        "It’s not stress that kills us, it is our reaction to it. – Hans Selye",
        "Almost everything will work again if you unplug it for a few minutes… even you. – Anne Lamott"
    ]
}

# ---- Output Section ----
st.header(f"Here’s something to help you if you're feeling {emotion}...")

# Quote
st.subheader("💬 Quote for You:")
st.success(random.choice(quotes[emotion]))

# Closing
st.markdown("---")
st.markdown("✨ Stay strong. You’re not alone. Keep moving forward. – Your AI Companion")
