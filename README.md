
# Flask Website Project

This is a simple website project built using Python's Flask framework. The project serves as an introductory example of how to create a basic web application using Flask, including rendering HTML templates, handling routes, and returning JSON responses.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Acknowledgement](#acknowledgements)

## Features

- **Home Page**: A basic home page that displays a personalized greeting.
- **Profile Page**: A simple profile page (template can be extended).
- **JSON Response**: A route that returns a JSON response for testing API functionality.
- **Redirection**: Demonstrates redirecting from one route to another.

## Installation

### Prerequisites

- Python 3.x
- Flask

### Steps

1. **Clone the repository**:
 

2. **Set up a virtual environment** (optional but recommended):
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install the dependencies**:
   ```bash
   pip install Flask
   ```

4. **Run the application**:
   ```bash
   python app.py
   ```
   The application will be available at `http://127.0.0.1:8000/`.

## Usage

- **Home Page**: Visit `http://127.0.0.1:8000/views/` to see the home page.
- **Profile Page**: Visit `http://127.0.0.1:8000/views/profile` to view the profile page.
- **JSON Response**: Visit `http://127.0.0.1:8000/views/json` to receive a JSON response.
- **Redirection**: Visit `http://127.0.0.1:8000/views/go-to-home` to be redirected to the home page.

### Example Code Snippets

Here’s a sample route that renders the home page:

```python
@views.route("/")
def home():
    return render_template("index.html", name="Joe", age=21)
```

This route demonstrates how to return a JSON response:

```python
@views.route("/json")
def get_json():
    return jsonify({'name': 'Joe', 'coolness': 21})
```

## Project Structure

```
flask-website/
│
├── app.py
├── views.py
├── templates/
│   ├── index.html
│   └── profile.html
└── static/
    └── index.js
```

- **`app.py`**: The main application file that initializes the Flask app.
- **`views.py`**: Contains all the routes and views for the application.
- **`templates/`**: Directory for HTML templates.
- **`static/`**: Directory for static files like JavaScript, CSS, and images.

## Acknowledgements

A special thanks to the 
Bytive YouTube channel for their invaluable tutorials and guidance. Their content played a significant role in helping to create and refine this project.