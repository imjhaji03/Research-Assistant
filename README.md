# Research Assistant AI


![Java](https://img.shields.io/badge/Java-17+-orange)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-brightgreen)
![Maven](https://img.shields.io/badge/Maven-4.0-blue)


A powerful browser-based tool designed to streamline your research process. Leveraging the power of Google's Gemini AI, this application can summarize long articles, extract key points, and perform other content operations directly in your browser.

---

## 🚀 Live Demo & Screenshots

Here is a look at the Research Assistant in action, summarizing a news article, and a view of the backend API being tested with Postman.

#### Frontend in Action

*The application's sidebar seamlessly integrates with any webpage, allowing for on-the-fly text summarization.*
<img src="images/chromeextension.png" alt="Extension View">


<br/>

#### Backend API Testing
*The robust Spring Boot backend handles the core logic, communicating with the Gemini API to process content. The endpoint is tested and validated using Postman.*
<img src="images/postmanapitest.png" alt="Api Testing">


---

## ✨ Core Features

*   **AI-Powered Summarization:** Instantly condense long articles and texts into concise summaries.
*   **Seamless Integration:** Works as a simple and intuitive sidebar in your browser.
*   **Extensible Operations:** The backend is designed to easily support more operations in the future (e.g., keyword extraction, tone analysis).
*   **Robust Backend:** Built with Java and Spring Boot for a scalable and reliable service.
*   **RESTful API:** A clear and well-defined API for processing requests.

---

## 🛠️ Tech Stack

This project is built with a modern and robust set of technologies:

*   **Backend:** Java 17, Spring Boot, Spring Web, Maven
*   **AI Service:** Google Gemini Pro API
*   **Frontend:** HTML, CSS, JavaScript
*   **Testing & Tools:** Postman, Git, IntelliJ IDEA

---

## ⚙️ Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

*   **Java Development Kit (JDK) 17** or newer.
*   **Apache Maven**
*   **Git** for version control.
*   A **Google Gemini API Key**. You can get one from [Google AI Studio](https://aistudio.google.com/app/apikey).

### Installation & Configuration

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/your_username/Reasearch-assistant.git
    cd Reasearch-assistant
    cd Reasearch-assistant_backend
    ```

2.  **Configure your API Key:**
    This project uses a `.env` file to manage secret keys securely. Create a new file named `.env` in the root directory of the project.

3.  **Add your API key to the `.env` file:**
    ```
    GEMINI_API_KEY=AIzaSyYOUR_REAL_API_KEY_HERE
    ```

4.  **Important:** Add the `.env` file to your `.gitignore` to ensure you don't commit your secret key to version control.
    ```gitignore
    # Ignore local environment variables
    .env
    ```

### Running the Application

1.  **Run the Spring Boot backend:**
    Use Maven to run the application. The server will start on `localhost:8080`.
    ```sh
    mvn spring-boot:run
    ```

2.  **Load the Frontend:**
    *This section depends on your frontend implementation. For a browser extension:*
    *   Open your browser (e.g., Chrome).
    *   Navigate to `chrome://extensions`.
    *   Enable "Developer mode".
    *   Click "Load unpacked" and select the frontend directory of this project.

---

## 📝 API Endpoint

The primary API endpoint for the application is documented below.

#### Process Text
- **POST** `/api/research/process`
- **Description:** Sends content and a requested operation to the backend for AI processing.
- **Request Body:**
  ```json
  {
      "content": "Your long text to be processed goes here...",
      "operation": "summarize"
  }
  ```
- **Success Response (200 OK):**
  ```json
  {
      "result": "The summarized version of your text appears here."
  }
  ```
## 🚀 Future Roadmap

This project is a living work, and I'm excited about its future potential. Some features I'm considering for future versions include:

*   **Keyword Extraction:** Automatically identify and list the most important terms in a text.
*   **Multi-Language Support:** Enable summarization for languages other than English.
*   **Custom Prompts:** Allow users to define their own operations beyond "summarize" (e.g., "Explain this to me like I'm five").
---
