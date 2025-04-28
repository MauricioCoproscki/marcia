# MarciaChart - AI Chat Application

A Django-based chat application that integrates with an AI API to provide ChatGPT-like functionality.

## Features

- User authentication (login/register)
- Chat history storage
- Real-time chat interface
- Modern and responsive UI
- SQLite database for data storage

## Setup

1. Clone the repository
2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file in the project root with the following content:
   ```
   API_KEY=your_api_key_here
   DEBUG=True
   SECRET_KEY=your-secret-key-here
   ```

5. Run migrations:
   ```bash
   python manage.py migrate
   ```

6. Create a superuser (optional):
   ```bash
   python manage.py createsuperuser
   ```

7. Run the development server:
   ```bash
   python manage.py runserver
   ```

8. Access the application at `http://127.0.0.1:8000`

## Usage

1. Register a new account or login with existing credentials
2. Start chatting with the AI
3. Your chat history will be saved and accessible from the sidebar

## Project Structure

- `marciachart/` - Main project configuration
- `chat/` - Chat application
  - `models.py` - Database models
  - `views.py` - View functions
  - `urls.py` - URL routing
- `templates/` - HTML templates
  - `base.html` - Base template
  - `chat/` - Chat-related templates
  - `registration/` - Authentication templates

## Security Notes

- Never commit your `.env` file
- Keep your API key secure
- Use strong passwords
- The application uses Django's built-in security features 