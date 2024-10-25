
## ***Installation***

Here the frontend and backend are separeted so lets dive in on the setup:

**Frontend**
```bash
  cd frontend
  npm i
```
Go to **.env.local**:

*Change The FastAPI Port or Use my Default Port 8900*
```env
    # You can use
    VITE_API_URL=http://localhost:YOUR_FASTAPI_PORT
```

**Backend**

Creating the virtual environment:
```bash
  cd backend
  python -m venv venv
  source venv/bin/activate
```

Installing Required modules:
```bash
  pip install -r requirements.txt
```

Go To **.env** and put your gemini api key:

*create one from here https://aistudio.google.com/app/apikey*
```env
GEMINI_API_KEY = YOUR_GEMINI_API_KEY
```

Go to **constants.py**:
```python
from dotenv import load_dotenv
import os
load_dotenv()

SERVER_URL = 'localhost'
PORT = '8900' # change port (frontend/.env.local also)
ENV = 'dev'
GEMINI_API_KEY = os.getenv('GEMINI_API_KEY')
```

**Now Lets run it:**
```bash
cd frontend
npm run dev
```

```bash
cd backend
py main.py
```

# **Thanks For Staying till the end!**
