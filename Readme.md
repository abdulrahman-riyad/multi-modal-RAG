# Multi-Modal RAG Chatbot

This project is a full-stack application that allows you to chat with your documents. It leverages a multi-modal Retrieval-Augmented Generation (RAG) pipeline, enabling it to understand both text and images within your uploaded PDF files.

The application features a modern, responsive frontend built with Next.js and a powerful, asynchronous Python backend using FastAPI.

## Key Features

-   **Multi-Modal Processing:** Extracts and understands both text and images from PDF documents.
-   **Chat with Your Documents:** Upload a file and ask questions about its content in a real-time chat interface.
-   **Modern Tech Stack:** Built with a clean separation between a Next.js frontend and a Python (FastAPI) backend.
-   **Asynchronous Backend:** Handles large file processing in the background without freezing the UI, providing a smooth user experience.
-   **Local Vector Storage:** Uses a local, file-based ChromaDB for efficient and private text retrieval.

## Technologies Used

-   **Frontend:** Next.js, React, TypeScript, Tailwind CSS, shadcn/ui
-   **Backend:** Python 3, FastAPI
-   **AI & Multi-Modality:**
    -   **LLM:** Google Gemini 2.5 Flash
    -   **PDF Parsing:** PyMuPDF
    -   **Image Handling:** Pillow
-   **Vector Database:** ChromaDB (Persistent Client)

## Local Setup and Installation

This project consists of two main parts: a Python backend and a Next.js frontend. You will need to run them in two separate terminals.

### Prerequisites

-   Python 3.12
-   Node.js 18.17+
-   A Google AI API Key

### Step 1: Clone the Repository

```bash
git clone https://github.com/abdulrahman-riyad/multi-modal-RAG.git
cd multi-modal-RAG
```

### Step 2: Configure Environment Variables

1.  Create a file named `.env` in the root of the project folder.
2.  Add your Google AI API key to it:

    ```env
    # Get your API key from Google AI Studio
    GOOGLE_API_KEY=YOUR_GOOGLE_API_KEY_HERE
    ```

### Step 3: Set Up and Run the Python Backend

1.  Navigate to the backend directory and create a virtual environment:

    ```bash
    cd python-ml-backend
    python -m venv venv
    # On Windows:
    venv\Scripts\activate
    # On macOS/Linux:
    # source venv/bin/activate
    ```

2.  Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

3.  Start the backend server (leave this terminal running):

    ```bash
    uvicorn app.main:app --host 0.0.0.0 --port 8001 --reload
    ```

### Step 4: Set Up and Run the Next.js Frontend

1.  Open a **new terminal**.
2.  Navigate to the frontend directory and install the dependencies:

    ```bash
    cd nextjs-app
    npm install
    ```

3.  Start the frontend development server (leave this terminal running):

    ```bash
    npm run dev
    ```

### Step 5: Open the Application

Your application is now running! Open your web browser and navigate to:

**[http://localhost:3000](http://localhost:3000)**
