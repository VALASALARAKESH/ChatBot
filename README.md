# ChatBot
This repository contains code for a chatbot that is built using Python, TensorFlow, and Flask. The chatbot model is trained on a dataset of text and responses, and it can be used to generate responses to a variety of prompts and questions. The chatbot also has a simple front-end that is built using HTML, CSS, and JavaScript. The chatbot can be locally hosted using Flask and Python.

The chatbot is designed to provide gadget suggestions and respond to user queries, greetings, and farewells on an eCommerce site. The chatbot utilizes a model trained on patterns and responses provided in the intents.json file.

# Repository Structure
1. ```intents.json``` : JSON file containing patterns and corresponding responses to train the chatbot model.

2. ```training.py``` : Python script used to train the chatbot model. It reads the intents.json file, preprocesses the data, and saves the trained model as 
                   ```chatbotmodel.h5```.

3. ```chatbot.py``` : Python script responsible for processing user input and generating responses using the trained chatbot model ```chatbotmodel.h5```.

4. ```classes.pkl``` : Pickle file that contains the list of classes/categories used in the chatbot.

5. ```words.pkl``` : Pickle file that contains the list of words used in the chatbot.

6. ```base.html``` : HTML file providing the structure of the chatbot interface.

7. ```styles.css``` : CSS file for styling the chatbot interface.

8. ```app.js``` : JavaScript file for handling user interactions and making API calls to the Flask backend.

9. ```app.py``` : Flask app script to locally host the chatbot at http://127.0.0.1:5000

# Getting Started

1. Clone the repository:
   ```
   git clone https://github.com/VALASALARAKESH/ChatBot.git

   cd ChatBot
   ```

2. Install the required Python packages:
   We want to create an Anaconda environment to run this chatbot and install TensorFlow, NLTK, NumPy, Flask, and Keras using Conda commands.
   
   1. Install Anaconda. You can download the latest version of Anaconda for your operating system from the Anaconda website: https://www.anaconda.com/download/.
      
   2. Create a new Conda environment. Open a terminal window and run the following command:
      ```
      conda create -n chatbot python=3.10
      ```
      This will create a new Conda environment called chatbot with Python 3.10 installed.
      
   3. Activate the Conda environment. Once the environment is created, you need to activate it before you can install any packages. To do this, run the following 
      command:
      ```
      conda activate chatbot
      ```
   4. Install the required packages. Now that the environment is activated, you can install the required packages by running the following commands:
      ```
      conda install tensorflow
      conda install nltk
      conda install numpy
      conda install flask
      conda install keras
      ```
   5. Verify the installation. Once the packages are installed, you can verify the installation by running the following commands:
      ```
      python -c "import tensorflow as tf"
      python -c "import nltk"
      python -c "import numpy"
      python -c "import flask"
      python -c "import keras"
      ```
      If you don't get any errors, then the packages have been installed successfully.
      
   6. Here is a python code that you can run to create the Conda environment and install the required packages:
      ```
      import os

      def create_conda_environment():
          """Creates a new Conda environment called `chatbot` with Python 3.8 installed."""
          os.system("conda create -n chatbot python=3.10")

      def activate_conda_environment():
          """Activates the `chatbot` Conda environment."""
          os.system("conda activate chatbot")
      
      def install_required_packages():
          """Installs the required packages for the chatbot."""
          os.system("conda install tensorflow")
          os.system("conda install nltk")
          os.system("conda install numpy")
          os.system("conda install flask")
          os.system("conda install keras")
      if __name__ == "__main__":
          create_conda_environment()
          activate_conda_environment()
          install_required_packages()

      ```
   7. You can save this code as a ```.py``` file and run it from the command line. For example, if you save the code as ```create_chatbot_environment.py```, you can run it by typing the following command into the terminal:
      ```
      python create_chatbot_environment.py
      ```
   8. This will create the Conda environment, activate it, and install the required packages.

3. Train the chatbot model by executing ```training.py```:
   
   ```python training.py```
4. Run the Flask app to host the chatbot locally:
   
   ```python app.py```
5. Visit http://127.0.0.1:5000 in your web browser to interact with the chatbot.
   
# How It Works
The chatbot works as follows:
  1. The `training.py` file is executed to create a chatbot model called `chatbotmodel.h5` using the `intents.json` file. The `intents.json` file contains patterns and responses that the chatbot can use to generate responses.
     
  2. The `chatbot.py` file creates two files called `classes.pkl` and `words.pkl`. These files are used to determine the response for a user query.

  3. The `app.py` file is used to host the chatbot locally at http://127.0.0.1:5000 using Flask.

  4. The user can interact with the chatbot by visiting the link http://127.0.0.1:5000 in their web browser.

  5. When the user enters a query, the chatbot first checks the `intents.json` file to see if there is a pattern that matches the query. If there is a match, the chatbot then uses the `chatbotmodel.h5` file to generate a response. If there is no match, the chatbot will try to generate a response based on the user's query.

  6. The `classes.pkl` file contains a list of classes that are used to classify user queries. The `words.pkl` file contains a list of words that are used to generate responses.

  7. The chatbot is hosted locally using Flask. Flask is a web framework that allows you to create web applications quickly and easily.
     

# Features of the Chatbot
1. **Gadget Suggestions:** The chatbot can suggest different gadgets to users based on their queries and preferences, providing personalized recommendations.

2. **Natural Language Processing (NLP):** Built using TensorFlow and Python, the chatbot leverages NLP techniques to understand and interpret user input, allowing for more natural and interactive conversations.

3. **Pattern-Based Responses:** The chatbot uses patterns and responses defined in the `intents.json` file to generate appropriate and contextually relevant answers to user queries, greetings, and farewells.

4. **Local Hosting:** The chatbot is locally hosted using Flask and Python, making it accessible on http://127.0.0.1:5000. This ensures that users can interact with the chatbot without requiring an internet connection.

5. **Frontend and Backend Separation:** The chatbot has a clear separation between the frontend and backend, allowing for easier maintenance and potential integration with different interfaces.

6. **User-Friendly Interface:** The chatbot is integrated into an eCommerce site, providing users with a familiar and intuitive interface to interact with the chatbot and get gadget recommendations.

7. **Training and Reusability:** The chatbot model is trained using the `training.py` script and saved as `chatbotmodel.h5`. Once trained, the model can be reused to handle user interactions efficiently.
8. **Flexibility:** The chatbot can be modified to meet your needs by changing the patterns and responses in the `intents.json` file.

# Limitations of the Chatbot
1. **Limited Vocabulary:** The chatbot's responses are based on the data provided in `intents.json`. If a user asks a question outside the defined intents, the chatbot may struggle to provide meaningful answers.
   
2. **Training Data Quality:** The performance of the chatbot heavily relies on the quality and diversity of the training data in `intents.json`. Insufficient or biased data may lead to inaccurate responses.
   
3. **Lack of Context Awareness:** While the chatbot can match patterns in user input, it may not fully grasp the context of the conversation. Consequently, the responses might lack context-awareness.
   
4. **No Real-Time Updates:** Since the chatbot is locally hosted, it may not receive real-time updates or improvements that could be available in cloud-based chatbot services.
   
5. **Language Limitations:** The chatbot's performance may vary depending on the complexity and nuances of the language used by the users. Slang or colloquial language might not be well-handled.
    
6. **No User Accounts:** The chatbot does not have user accounts or profiles, limiting its ability to provide personalized responses based on historical user interactions.
    
7. **No External Data Retrieval:** The chatbot is confined to the information available within the intents.json file and cannot retrieve real-time data from external sources.
    
8. **Performance and Scalability:** As the chatbot runs locally, it may face performance issues and may not be as scalable as cloud-based solutions, especially when handling a large number of concurrent users.

# Contributing
If you would like to contribute to the chatbot, please feel free to fork the repository and submit a pull request.

# Contact
If you have any questions about the chatbot, please feel free to open an issue in the repository or contact me at `valasalarakesh1254@gmail.com`.





   
      







