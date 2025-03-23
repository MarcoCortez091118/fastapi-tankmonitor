# ⚙️ Tank Monitor FastAPI backend

## 🧾 Description
This is a backend built with FastAPI and connected to Firebase Firestore,
an integration for the project "Tank Monitor". It provides REST endpoints
and cloud database connectivity.

[🔗 Frontend repository](https://github.com/MarcoCortez091118/react-tankmonitor-ui-chakra)

## How to use it
**Step 1** - Clone the project

```bash
git clone https://github.com/MarcoCortez091118/fastapi-tankmonitor.git
cd fastapi-tankmonitor
```

**Step 2** - Create and run a virtual enviroment
```bash
python -m venv venv

# On Windows
.\venv\Scripts\activate

# On Mac/Linux
source venv/bin/activate
```

**Step 3** - Install dependencies
```bash
pip install -r requirements.txt
```

**Step 4** - Setup the backend locally

To run the backend locally, you need to provide Firebase service account credentials. 
These credentials are required for authentication and Firebase Admin SDK integration.

1. Place your Firebase service account JSON file inside the `app/` directory and name
it `firebase_key.json` (or ask the backend developer for that file).
2. Create a `.env` file (use the `.env.example` provided).

**Step 5** - Start development server
```bash
uvicorn app.main:app --reload
```
* Visit: http://localhost:8000
* Docs
  - Swagger UI: http://localhost:8000/docs
  - Redoc: http://localhost:8000/redoc

## 🔌 Test the backend from frontend
Using fetch:
```javascript
fetch("http://localhost:8000/")
  .then(res => res.json())
  .then(data => console.log(data));
```
Using axios:
```javascript
import axios from "axios";

axios.get("http://localhost:8000/")
  .then(res => console.log(res.data));
```