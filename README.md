# AI-Chatbot-project
Initial scaffold generated using AI,extended with custom features
This is a simple AI chatbot built using Python and PostgreSQL for database.

## tech Used
-Python
-Postgre SQL
Open Al/Claude API

## Note
Initial structure generated with AI and further customized by me.

## How it Works
-- Install Python + PostgreSQL          One dedicated PC on the LAN
-- Set static IP on that PC             eg: 192.168.1.100
-- All other PCs access via Browser     http://192.168.1.100:8000/admin
-- Fingrerprint machine connects to     same LAN,points to 192.168.1.100

**Step 1- Create local database**
#Linux/Mac
./scripts/setup_db.sh
#Windows - open psql as postgres and run:
psql -U pstgres -f scripts/setup_db.sql

**Step 2 -Edit** .env with your fingerprint machine IP

DEVICE_IP=192.168.1.201   <- change this
SECRET_KEY = any_long_random_string

**Step 3 - Install & run**
python -m venv venv
source venv/bin/activate      #Windows: venv\Scripts\activate
pip install -r requirements.txt
alembic upgrade head          # create tables
python run.py                 # start server


**Admin Panel**

http://localhost:8000/admin

username : admin
password :admin123
