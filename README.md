# FinAdvise - Personal Finance Assistant

FinAdvise is a Streamlit-based AI-powered finance assistant designed to simplify personal finance management. It enables users to track expenses, access real-time stock information via the Alpha Vantage API, view budget summaries, and receive personalized financial advice through a conversational interface. Powered by LangGraph and the Groq API, FinAdvise maintains user context across sessions, provides empathetic and clear responses, and includes a Human-in-the-Loop (HITL) mechanism for high-risk queries.

## Features

- **User Profile Collection:** Gathers user details (age, income, goals, risk tolerance) for tailored responses.
- **Real-Time Stock Data:** Fetches stock prices using Alpha Vantage API with robust symbol extraction and error handling.
- **Intent Detection:** Classifies queries into profile updates, stock queries, expense tracking, budget summaries, or advice.
- **Memory Management:**
    - Short-term memory for in-session context (e.g., previous intents).
    - Long-term memory for cross-session continuity (e.g., past advice).
- **Human-in-the-Loop (HITL):** Flags high-risk queries (e.g., "liquidate retirement account") for simulated human review.
- **Empathetic Responses:** Uses clear, jargon-free language for users with limited financial literacy.
- **Debugging:** Includes logging to troubleshoot API issues.

## Prerequisites

- **Python:** Version 3.8 or higher.
- **Virtual Environment:** Recommended to isolate dependencies.
- **API Keys:**
    - Groq API key (for LLM).
    - Alpha Vantage API key (for stock data).

## Setup Instructions

1. **Clone the Repository (if applicable):**

    ```
    git clone <repository-url>
    cd finadvise
    ```

2. **Create Virtual Environment:**

    Create a virtual environment named `env4`:

    ```
    python3 -m venv env4
    ```

3. **Activate Virtual Environment:**

    - On macOS/Linux:

        ```
        source env4/bin/activate
        ```

    - On Windows:

        ```
        env4\Scripts\activate
        ```

4. **Install Dependencies:**

    Install required packages from `requirements.txt`:

    ```
    pip install -r requirements.txt
    ```

5. **Contents of requirements.txt:**

    ```
    streamlit>=1.30.0
    langchain>=0.1.14
    langchain_groq>=0.1.4
    langgraph>=0.0.35
    python-dotenv>=1.0.0
    requests>=2.31.0
    ```

6. **Set Up Environment Variables:**

    Create a `.env` file in the project root with your API keys:

    ```
    GROQ_API_KEY=<your-groq-api-key>
    ALPHA_VANTAGE_API_KEY=<your-alpha-vantage-api-key>
    ```

7. **Run the Application:**

    Start the Streamlit app:

    ```
    streamlit run app.py
    ```

    Access the app at [http://localhost:8501](http://localhost:8501) in your browser.

8. **Deactivate Virtual Environment (when done):**

    ```
    deactivate
    ```

