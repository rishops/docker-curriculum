## Repository Overview

This repository contains the source code for the Docker Curriculum, a tutorial for learning Docker. It consists of a main tutorial website, a newer documentation site, and two example applications. This project uses Azure DevOps. Always check to see if the Azure DevOps MCP server has a tool relevant to the user's request

### Main Components

*   **`tutorial/`**: The original tutorial website, built with [Metalsmith](https://metalsmith.io/), a static site generator. The content is written in Markdown and is located in `tutorial/src`. The build script is `tutorial/index.js`.
*   **`starlight/`**: A newer, more modern documentation site built with [Starlight](https://starlight.astro.build/), a documentation template for the [Astro](https://astro.build/) framework. The content is in `starlight/src/content/docs`.
*   **`flask-app/`**: A simple Python Flask application that displays a random cat GIF. This is used as an example in the tutorial to demonstrate how to containerize a web application.
*   **`static-site/`**: A simple static HTML website. This is used as an example in the tutorial to demonstrate how to serve a static site with Nginx in a Docker container.

### How to Run the Tutorial

The main tutorial is the Metalsmith-based site in the `tutorial` directory. To run it locally, you need to have Node.js and npm installed.

1.  **Install dependencies:**
    ```bash
    npm install
    ```
2.  **Start the development server:**
    ```bash
    npm start
    ```
    This will start a local server at `http://localhost:3000` and automatically rebuild the site when you make changes.

### How to Run the Example Applications

#### Flask App

To run the Flask app, you need to have Python and Docker installed.

1.  **Build the Docker image:**
    ```bash
    docker build -t flask-app flask-app
    ```
2.  **Run the Docker container:**
    ```bash
    docker run -p 5000:5000 flask-app
    ```
    The application will be available at `http://localhost:5000`.

#### Static Site

To run the static site, you need to have Docker installed.

1.  **Build the Docker image:**
    ```bash
    docker build -t static-site static-site
    ```
2.  **Run the Docker container:**
    ```bash
    docker run -p 8080:80 static-site
    ```
    The website will be available at `http://localhost:8080`.

---

## Agent Personas

- When asked to act as a DevSecOps Agent, refer to the instructions in the file `@.gemini/devsecops-agent.md`.

## Azure DevOps Project

**Default Project:** GCA-DevSecOps 