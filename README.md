# Scam Message Investigator

### AI-Powered Scam Detection System

## Project Overview

Scam Message Investigator is an AI-powered application designed to analyze suspicious text messages, emails, and chats to identify potential scams and security threats.

The application uses a locally running Large Language Model (LLM) through Ollama to investigate messages and generate detailed risk assessments.

It identifies suspicious patterns such as urgent threats, fraudulent links, requests for personal information, upfront payments, impersonation, and unrealistic offers.

Built using Python and Streamlit, the application provides an interactive interface where users can investigate messages, analyze potential risks, and receive practical safety recommendations.

## Objectives

* Identify potentially fraudulent messages using AI.
* Analyze suspicious keywords, phrases, and links.
* Classify messages based on their risk levels.
* Highlight suspicious evidence directly in the original message.
* Provide practical recommendations to avoid online scams.
* Maintain privacy by processing messages locally through Ollama.

## Key Features

### 1. AI-Powered Scam Detection

Uses a locally running LLM to analyze messages and identify potential scam indicators.

### 2. Risk Assessment

Classifies messages into three risk categories:

* Low Concern
* Medium Concern
* High Concern

Generates a risk score between 0 and 100.

### 3. Warning Sign Identification

Detects suspicious elements such as:

* Urgent threats and account-blocking messages.
* Requests for OTP, passwords, PINs, and banking information.
* Suspicious links and downloads.
* Fake job offers and registration fees.
* Unrealistic financial promises.
* Impersonation attempts.

### 4. Evidence Highlighting

Highlights suspicious phrases found in the original message and explains why they may indicate fraudulent activity.

### 5. Reassuring Signs

Identifies elements that may support a legitimate interpretation of the message.

### 6. Safety Recommendations

Provides actionable suggestions to help users avoid potential online fraud.

### 7. Sample Messages

Includes predefined examples for testing:

* KYC / Bank Block
* Job Offer Fee
* Normal Delivery Update

### 8. JSON Report Download

Allows users to download the AI-generated analysis report in JSON format.

### 9. Local AI Processing

Uses Ollama to run AI models locally instead of depending on cloud-based AI APIs.

## Technologies Used

| Technology          | Purpose                                      |
| ------------------- | -------------------------------------------- |
| Python              | Core programming language                    |
| Streamlit           | Web application interface                    |
| Ollama              | Local LLM execution                          |
| Gemma 3 (1B)        | AI-based message analysis                    |
| Requests            | Communication with Ollama API                |
| JSON                | Structured AI response and report generation |
| Regular Expressions | JSON parsing and evidence matching           |
| HTML                | Highlighting suspicious phrases              |

## System Architecture

```text
             User
               |
               v
     Enter Suspicious Message
               |
               v
          Streamlit UI
               |
               v
         Python Backend
               |
               v
           Ollama API
               |
               v
            Gemma 3
               |
               v
        Message Analysis
               |
               v
         Risk Assessment
               |
        +------+------+
        |             |
        v             v
   Warning Signs   Reassuring Signs
        |             |
        +------+------+
               |
               v
    Safety Recommendations
               |
               v
        Results Display
               |
               v
       Download JSON Report
```

## Installation and Setup

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/Scam-Message-Investigator.git
```

### Step 2: Navigate to the Project Directory

```bash
cd Scam-Message-Investigator
```

### Step 3: Install Required Libraries

```bash
pip install streamlit requests
```

### Step 4: Install Ollama

Download and install Ollama:

https://ollama.com/

### Step 5: Download the AI Model

```bash
ollama pull gemma3:1b
```

### Step 6: Run the Application

Make sure Ollama is running, then execute:

```bash
streamlit run app.py
```

The application will open in your default web browser.

## Project Structure

```text
Scam-Message-Investigator/
│
├── app.py
│
├── README.md
│
└── requirements.txt
```

## How It Works

1. The user enters a suspicious message into the Streamlit application.
2. The application sends the message to the locally running Ollama API.
3. The selected language model analyzes the message using a predefined system prompt.
4. The model generates a structured JSON response containing the risk level, risk score, warning signs, and recommendations.
5. Python processes the response and validates suspicious evidence against the original message.
6. The application displays the analysis and highlights verified suspicious phrases.
7. Users can download the analysis report in JSON format.

## Privacy and Security

* Uses locally hosted AI models through Ollama.
* Does not require an external AI API key.
* Treats submitted messages as untrusted input.
* Verifies whether suspicious evidence actually exists in the original message.
* Does not assume every message is fraudulent.
* Clearly communicates the limitations of AI-generated assessments.

## Limitations

* AI-generated results may not always be accurate.
* A message alone cannot establish whether a sender or link is genuine.
* The application does not independently verify URLs, phone numbers, or sender identities.
* Local model performance depends on available system resources.
* Users should verify important information through official communication channels.

## Future Enhancements

* Add multilingual scam message detection.
* Integrate URL reputation checking.
* Implement phishing email detection.
* Add SMS and email analysis support.
* Maintain a history of previously analyzed messages.
* Improve detection accuracy using specialized scam datasets.
* Add visual analytics for scam categories and risk statistics.

## Learning Outcomes

Through this project, I gained practical experience in:

* Integrating Large Language Models into Python applications.
* Working with Ollama and local AI models.
* Building interactive applications using Streamlit.
* Designing structured prompts for AI-based analysis.
* Processing JSON responses from LLMs.
* Implementing evidence verification and text highlighting.
* Understanding AI applications in cybersecurity.

## Disclaimer

This application provides an AI-generated preliminary risk assessment. It is not a substitute for professional cybersecurity investigation. Always verify suspicious messages through official websites, applications, or customer support channels before taking action.

## Author

**Doddi. Hasini**

B.Sc. Computer Science with Artificial Intelligence

**Project Name:** Scam Message Investigator
