# PyBot.py
from datetime import datetime

print("====================================")
print("      PYTHON RULE-BASED CHATBOT")
print("====================================")
print("Type 'exit' to close the chatbot.\n")


def chatbot_response(user_input):

    user_input = user_input.lower().strip()

    # Greetings
    if "hello" in user_input or "hi" in user_input:
        return "Hi there! Nice to meet you. How can I assist you?"

    elif "how are you" in user_input:
        return "I'm doing great! Thanks for asking."

    elif "your name" in user_input:
        return "My name is PyBot, a simple chatbot built with Python."

    elif "who made you" in user_input or "developer" in user_input:
        return "I was developed as a Python chatbot project."

    elif "ai" in user_input:
        return "Artificial Intelligence enables computers to perform tasks that usually require human intelligence."

    elif "python" in user_input:
        return "Python is a powerful and beginner-friendly programming language."

    elif "time" in user_input:
        current_time = datetime.now().strftime("%I:%M %p")
        return f"The current time is {current_time}."

    elif "date" in user_input:
        current_date = datetime.now().strftime("%d-%m-%Y")
        return f"Today's date is {current_date}."

    elif "day" in user_input:
        current_day = datetime.now().strftime("%A")
        return f"Today is {current_day}."

    elif "favorite color" in user_input:
        return "I like green because it represents growth and innovation."

    elif "thank" in user_input:
        return "You're most welcome! Happy to help."

    elif "help" in user_input:
        return "You can ask me about AI, Python, time, date, day, or simply chat with me."

    elif "bye" in user_input or "exit" in user_input:
        return "Goodbye! Have a wonderful day."

    else:
        return "Sorry, I don't have an answer for that yet."


while True:

    user_message = input("You: ")

    response = chatbot_response(user_message)

    print("Bot:", response)

    if "bye" in user_message.lower() or "exit" in user_message.lower():
        break
