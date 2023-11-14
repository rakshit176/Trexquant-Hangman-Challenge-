# Trexquant-Hangman-Challenge-
The method in ipynb file defines a Python class `HangmanAPI` that serves as an interface for interacting with a Hangman game API. Here's an overview of the main components and functionality:

1. **Initialization:**
   - The class is initialized with parameters such as `access_token`, `session`, and `timeout`.
   - It determines the Hangman game API URL using the `determine_hangman_url` method.

2. **Building Dictionaries:**
   - It reads a full dictionary of words from a file and builds various dictionaries based on word length using methods like `build_dictionary` and `build_n_word_dictionary`.
   - The `full_dictionary_common_letter_sorted` attribute contains a counter of the most common letters in the full dictionary.

3. **Word and Letter Processing:**
   - The class has methods for counting vowels in a word (`vowel_count`) and processing words and letters to filter dictionaries (`func`, `func2`).

4. **Game Logic:**
   - The `guess` method is the core of the Hangman game logic. It makes educated guesses based on the current state of the game and the dictionaries.
   - The `start_game` method initiates a new Hangman game, makes guesses, and handles responses until the game is either successful or fails.

5. **API Communication:**
   - The class has a `request` method to make HTTP requests to the Hangman API using the `requests` library.
   - It handles errors using a custom exception class `HangmanAPIError`.

6. **Exception Handling:**
   - The `HangmanAPIError` class is defined to handle errors returned by the Hangman API.

7. **Other Methods:**
   - The `my_status` method retrieves the current status of the Hangman game.

Overall, this class encapsulates the functionality needed to interact with a Hangman game API, from initializing the game to making guesses and handling responses. The code is structured and provides comments for clarity. If you have specific questions or if there's a particular part you'd like more explanation on, feel free to ask!
