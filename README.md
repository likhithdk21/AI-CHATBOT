# AI-CHATBOT
Chatty is a simple Python chatbot that replies to greetings, jokes, facts, fitness tips, and help requests using keyword matching. Great for beginners to learn Python basics like functions, loops, and conditionals.
#CODE UDED FOR CHATBOT
# import useful libraries
import random

# define some sample responses
greeting = [
    "Hello! How can I assist you today?",
    "Hi there! What can I do for you?",
    "Greetings! How may I help you?",
    "Hey! What brings you here today?",
    "Hello! How can I help you?"
]

help_response = [
    "I can help you with a variety of tasks. What do you need assistance with?",
    "I can tell you some fun facts.",
    "I can tell you a joke."
]

jokes = [
    "Why did the scarecrow win an award? Because he was outstanding in his field!",
    "Why don't scientists trust atoms? Because they make up everything!",
    "What do you call fake spaghetti? An impasta!",
    "Why did the bicycle fall over? Because it was two-tired!"
]

fun_facts = [
    "Did you know that honey never spoils? Archaeologists have found pots of honey in ancient Egyptian tombs that are over 3000 years old and still edible.",
    "Bananas are berries, but strawberries aren't!",
    "Octopuses have three hearts!",
    "A group of flamingos is called a 'flamboyance'."
    
]
fitness=["Do at least 30 minutes of activity 5 days a week.Mix cardio (like walking, jogging, cycling) with strength training (like push-ups, weight lifting).",
         "Stay hydrated! Drink plenty of water throughout the day, especially before, during, and after exercise.",
         "Get enough sleep! Aim for 7-9 hours of quality sleep each night to help your body recover and stay energized.",
         "Incorporate flexibility exercises like stretching or yoga to improve your range of motion and prevent injuries.",
         "Set realistic fitness goals and track your progress to stay motivated and accountable."]

# function to generate a response based on user input
def chatty_response(user_input):
    user_input = user_input.lower()
    
    if any(greet in user_input for greet in ["hello", "hi", "hey", "greetings"]):
        return random.choice(greeting)
    elif "joke" in user_input:
        return random.choice(jokes)
    elif "fact" in user_input:
        return random.choice(fun_facts)
    elif "help" in user_input:
        return random.choice(help_response)
    elif "fitness" in user_input:
        return random.choice(fitness)
    elif "your name" in user_input or "who are you" in user_input:
        return "I am Chatty, your friendly chatbot here to assist you!"
    elif "what's up" in user_input or "how are you" in user_input:
        return "I'm just a program, but I'm here and ready to help you!"
    elif"how are you" in user_input:
        return "I'm just a program, but I'm here and ready to help you!"
    else:
        return "I'm not sure how to respond to that. You can ask me for help, a joke, or a fun fact! or fitness tips "

# main function to run the chatbot
def chatbot():
    print("Welcome to Chatty the Chatbot! I am here to help you.")
    print("Type 'bye' to exit the chatbot.")

    while True:
        user_input = input("You: ")
        if user_input.lower() == 'bye':
            print("Chatty: Goodbye! Have a great day!")
            break
        else:
            response = chatty_response(user_input)
            print("Chatty:", response)

# running the chatbot
if __name__ == "__main__":
    chatbot()

