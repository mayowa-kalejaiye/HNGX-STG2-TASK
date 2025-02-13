# FastAPI Book Management API

## Project Description

This FastAPI application provides a robust RESTful API for managing a personal book collection. With integrated CRUD functionalities, input validation via Pydantic, comprehensive error handling, and auto-generated documentation, the service is tailored for local development.

## Features Overview

- Manage your books: Create, Read, Update, Delete (CRUD)
- Leverage Pydantic for input validation
- Enum-based genre management
- Full test suite via pytest
- Auto-generated docs with Swagger UI & ReDoc
- CORS security included

## Project Layout

fastapi-book-project/
 ├── api/ 
 │ ├── db/ 
 │ │ ├── __init__.py 
 │ │ └── schemas.py  // Data models and in-memory DB
 │ ├── routes/ 
 │ │ ├── __init__.py 
 │ │ └── books.py  // Endpoint handlers for books
 │ └── router.py  // API router configuration
 ├── core/ 
 │ ├── __init__.py 
 │ └── config.py  // Application settings
 ├── tests/ 
 │ ├── __init__.py 
 │ └── test_books.py  // Endpoint tests
 ├── main.py  // Application entry point
 ├── requirements.txt  // Dependencies
 └── README.md

## Technologies Used

- Python 3.12
- FastAPI
- Pydantic
- pytest
- uvicorn

## Setup Instructions

1. Open a terminal in:
   c:/path/to/your/project
2. Create a virtual environment:
   python -m venv venv
   // Activate the virtual environment:
   venv\Scripts\activate (Windows) or source venv/bin/activate (Unix)
3. Install the dependencies:
   pip install -r requirements.txt

## Starting the Server

Run the following command to launch the API:
   uvicorn main:app

Access the documentation at:
   Swagger UI: http://localhost:8000/docs
   ReDoc: http://localhost:8000/redoc

## API Endpoints

### Books
- GET /api/v1/books/ : Fetch all books
- GET /api/v1/books/{book_id} : Fetch a specific book
- POST /api/v1/books/ : Add a new book
- PUT /api/v1/books/{book_id} : Update an existing book
- DELETE /api/v1/books/{book_id} : Delete a book

### Health Check
- GET /healthcheck : Verify API status

## Example Request Payload

```json
{
  "id": 1,
  "title": "Book Title",
  "author": "Author Name",
  "publication_year": 2024,
  "genre": "Fantasy"
}
```

## Supported Genres

- Science Fiction
- Fantasy
- Horror
- Mystery
- Romance
- Thriller

## Testing

Execute tests with:
   pytest

## Error Handling

The API manages errors for:
- Non-existent books
- Invalid identifiers and genres
- Malformed inputs

## Contribution Guidelines

1. Fork the repository.
2. Create a feature branch: git checkout -b feature/MyFeature.
3. Commit your changes.
4. Push your branch.
5. Submit a Pull Request.

## License

Distributed under the MIT License. See LICENSE for details.

## Support

For issues or inquiries, please open an issue in the GitHub repository.