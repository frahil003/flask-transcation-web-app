# Flask Transaction Web App

A simple Flask web application for managing transaction records.

This project demonstrates the basic CRUD workflow in Flask using server-side rendered HTML templates.  
It is intended as a learning project to practice Flask routing, form handling, template rendering, and basic application structure.

## Features

- View all transactions
- Add a new transaction
- Edit an existing transaction
- Delete a transaction
- Render HTML pages with Flask templates
- Simple Bootstrap-based UI

## Tech Stack

- Python
- Flask
- HTML
- Bootstrap 4

## Project Structure

```text
flask-transcation-web-app/
├── app.py
├── requirements.txt
├── .gitignore
└── templates/
    ├── transactions.html
    ├── form.html
    ├── edit.html
    └── search.html
```

## How It Works

The application stores transactions in a simple in-memory Python list inside `app.py`.

Each transaction contains:

- id
- date
- amount

Because no database is used yet, all data is reset whenever the application restarts.

## Installation

1. Clone the repository:

git clone https://github.com/frahil003/flask-transcation-web-app.git
cd flask-transcation-web-app

2. Create a virtual environment:

python3 -m venv .venv

3. Activate the virtual environment:

source .venv/bin/activate

4. Install dependencies:

pip install -r requirements.txt

## Run the Application

Start the Flask app with:

python app.py

The application will run locally at:

http://127.0.0.1:5000

## Available Routes

| Route                      | Methods   | Description                  |
| -------------------------- | --------- | ---------------------------- |
| `/`                        | GET       | Display all transactions     |
| `/add`                     | GET, POST | Add a new transaction        |
| `/edit/<transaction_id>`   | GET, POST | Edit an existing transaction |
| `/delete/<transaction_id>` | GET       | Delete a transaction         |

## Example Data

The application starts with three sample transactions:

- 2023-06-01 → 100
- 2023-06-02 → -200
- 2023-06-03 → 300

## Notes

- This project uses in-memory storage only
- Data will not persist after restarting the app
- The search functionality is prepared but not yet implemented

## Learning Goals

This project is useful for learning and practicing:

- Flask basics
- Routing
- Handling forms with request.form
- Redirects with redirect() and url_for()
- Rendering templates with render_template()
- Building a simple CRUD web app

## Possible Improvements

- Add persistent storage with SQLite or PostgreSQL
- Implement transaction search functionality
- Add input validation
- Add flash messages for better UX
- Refactor into a package structure
- Add tests
- Use POST for delete actions instead of GET
- Prepare the app for production deployment

## License

This project is for educational and learning purposes.
