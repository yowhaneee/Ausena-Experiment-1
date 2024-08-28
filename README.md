## PA 1.1
ALPHABET SOUP PROBLEM: Create a function that takes a string and returns a string with its letters in alphabetical order.

    def alphabet_soup():
        # Make the user input a word
        input_string = input("Enter a word: ")
        
        # Convert the string to lowercase
        input_string = input_string.lower()
        
        # Initialize an empty string to store the sorted characters
        sorted_string = ""
        
        # Loop through each character in the alphabet
        for current_char in range(ord('a'), ord('z') + 1):
            # Loop through each character in the input string
            for char in input_string:
                # If the current character in the alphabet matches the character in the input string
                if chr(current_char) == char:
                    # Add the character to the sorted string
                    sorted_string += char
        
        # Print the sorted string
        print("Alphabetical order:", sorted_string)
    
    # Call the function to execute
    alphabet_soup()

## PA 1.2
EMOTICON PROBLEM: Create a function that changes specific words into emoticons. Given a sentence as a string, replace the words smile, grin, sad and mad with their corresponding emoticon:

    def emotify():
        # Make the user input a sentence
        sentence = input("Enter a sentence: ")
    
        # Define a dictionary with words as keys and their corresponding emoticons as values
        emoticon_dict = {
            "smile": ":)",
            "grin": ":D",
            "sad": ":((",
            "mad": ">:("
        }
        
        # Split the sentence into words
        words = sentence.split()
        
        # Replace words with their corresponding emoticons
        for i in range(len(words)):
            if words[i] in emoticon_dict:
                words[i] = emoticon_dict[words[i]]
        
        # Join the words back into a single string
        emotified_sentence = " ".join(words)
        
        # Print the emotified sentence
        print("Emotified sentence:", emotified_sentence)
    
    # Call the function to execute
    emotify()

## PA 1.3
UNPACKING LIST PROBLEM: Unpack the list writeyourcodehere into three variables, being first, middle, and last, with middle being everything in between the first and last element. Then print all three variables.

    def unpack_list():
        # Prompt the user to enter a list of numbers separated by commas
        input_string = input("Enter a list of numbers separated by commas (e.g., 1,2,3,4,5,6): ")
        
        # Convert the input string to a list of integers
        # First, split the string by commas, then convert each split value to an integer
        lst = [int(x) for x in input_string.split(',')]
        
        # Check if the list has at least 3 elements
        if len(lst) < 3:
            print("The list must contain at least 3 elements.")
            return
        
        # Unpack the list into variables
        # Use unpacking with the * operator to capture the middle elements
        first, *middle, last = lst
    
        # Sort the middle numbers from least to greatest
        middle.sort()
        
        # Print the variables
        print("first:", first)
        print("middle:", middle)
        print("last:", last)
    
    # Call the function to run the program
    unpack_list()
