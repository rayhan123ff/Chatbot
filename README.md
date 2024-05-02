# Chatbot
This a chatbot make with python code.
import nltk
from nltk.chat.util import Chat, reflections

# Define pairs of patterns and responses
pairs = [
    [
        r"hi|hello|hey",
        ["Hello!", "Hey there!", "Hi!"]
    ],
    [
        r"how are you?",
        ["I'm doing well, thank you!", "I'm good, thanks for asking!"]
    ],
    [
        r"what is your name?",
        ["I'm a chatbot.", "You can call me Chatbot."]
    ],
    [
        r"quit",
        ["Bye! Take care.", "Goodbye!"]
    ],
]

# Create a chatbot with the defined patterns
def chatbot():
    print("Hi! I'm a chatbot. How can I help you today?")
    chat = Chat(pairs, reflections)
    chat.converse()

# Main function to run the chatbot
def main():
    nltk.download('punkt')  # Download necessary NLTK data
    chatbot()

if __name__ == "__main__":
    main()
