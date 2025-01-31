# FastAPI Factorial API

## Description
This is a simple FastAPI application that calculates the factorial of a given number. The API exposes a single endpoint to compute the factorial of a non-negative integer.

## Features
- Computes the factorial of a given number.
- Returns JSON responses.
- Simple and lightweight.

## Installation

### Prerequisites
- Python 3.7+

### Setup
1. Clone the repository:
   ```sh
   git clone <repository_url>
   cd <repository_name>
   ```
2. Create a virtual environment (optional but recommended):
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```
3. Install dependencies:
   ```sh
   pip install fastapi uvicorn
   ```

## Usage

### Running the API
Start the FastAPI application with Uvicorn:
```sh
uvicorn main:app --reload
```

### API Endpoint
#### Get Factorial
**Request:**
```
GET /factorial/{starting_number}
```
- `starting_number` (int): The number for which to calculate the factorial.

**Response:**
- If `starting_number == 0`, returns:
  ```json
  {"result": false}
  ```
- Otherwise, returns:
  ```json
  {
      "starting_number": <input_number>,
      "factorial": <calculated_factorial>
  }
  ```

### Example Usage
Using `curl`:
```sh
curl -X GET "http://127.0.0.1:8000/factorial/5"
```
Expected Response:
```json
{
    "starting_number": 5,
    "factorial": 120
}
```

## License
This project is licensed under the MIT License.

