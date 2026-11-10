# HotelOps AI – Smart Hotel Operations Assistant

## Project Overview
HotelOps AI is an AI-powered assistant designed to help hotel employees handle everyday operational tasks. Employees can enter requests in natural language, and the AI interprets the request and performs the appropriate action.

The goal of this project is to make common hotel tasks easier, faster, and more organized.

## Features
- **Housekeeping Management:** Divides rooms equally among housekeepers.
- **Register Calculator:** Calculates register balances using safe arithmetic operations.
- **Shift Reports:** Creates and saves hotel shift reports.
- **Read Reports:** Opens and displays previously saved reports.
- **File Management:** Lists saved files in the hotel workspace.
- **Folder Creation:** Creates folders within the hotel workspace.
- **Activity Logging:** Records actions, timestamps, and success or error status.

## AI Agent and Prompt Engineering
HotelOps AI uses the Groq API to interpret natural-language requests and determine which action should be performed.

Prompt engineering techniques include:
- **Role-Based Prompting:** Defines the AI as a hotel operations assistant.
- **Structured Output Prompting:** Requires the AI to return structured JSON containing an action, parameters, and message.
- **Constraint-Based Prompting:** Limits the AI to a predefined list of supported actions.
- **Action Validation:** Checks the AI response before executing an operation.

## Safety and Error Handling
- Only approved actions can be executed.
- Arithmetic calculations use a restricted evaluator instead of unsafe code execution.
- Reports are saved as text files inside a designated workspace.
- Existing report files cannot be overwritten.
- Invalid requests and execution errors are handled and logged.
- Activity logs record the actions performed by the agent.

## Technologies Used
- Python
- Flask
- Groq API
- HTML, CSS, and JavaScript
- JSON
- Gunicorn

## Run Locally

1. Clone or download this repository.
2. Install the required packages:

   `pip install -r requirements.txt`

3. Create a `.env` file in the project directory and add your Groq API key:

   `GROQ_API_KEY=your_groq_api_key_here`

4. Start the application:

   `python app.py`

5. Open `http://127.0.0.1:5000` in your browser.

## Project Purpose
This project demonstrates how a large language model can interpret user requests and connect them to real actions through an AI agent, rather than simply generating text responses.
