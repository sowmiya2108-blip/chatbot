# chatbot
import re

def chatbot():
    print("ChatBot: Hello! I'm a simple chatbot. Type 'exit' to quit.")

    while True:
        user_input = input("You: ").lower()

        # Exit condition
        if user_input == "exit":
            print("ChatBot: Goodbye! Have a nice day!")
            break

        # Rule-based responses using if-else and pattern matching
        if re.search(r'\b(hi|hello|hey)\b', user_input):
            print("ChatBot: Hi there! How can I help you?")
        elif re.search(r'\bhow are you\b', user_input):
            print("ChatBot: I'm just a bot, but I'm doing fine. How about you?")
        elif re.search(r'\bwhat is your name\b', user_input):
            print("ChatBot: I'm a simple rule-based chatbot created in Python.")
        elif re.search(r'\bhelp\b', user_input):
            print("ChatBot: You can greet me, ask how I am, or ask for my name.")
        elif re.search(r'\bthank(s| you)?\b', user_input):
            print("ChatBot: You're welcome!")
        elif re.search(r'\bbye\b', user_input):
            print("ChatBot: Bye! Come back soon.")
            break
        else:
            print("ChatBot: I'm sorry, I don't understand. Can you rephrase?")

# Run the chatbot
chatbot()
