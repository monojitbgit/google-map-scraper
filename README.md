# 🗺️ Google Maps Data Scraper (Python + Selenium + Google Sheets)

This project automates **Google Maps business data extraction** using **Selenium WebDriver** and stores the collected information directly in a **Google Sheet**.  

It retrieves business names, phone numbers, addresses, plus codes, and websites for given search queries — all handled automatically, with results saved in real-time.

---

## Key Features

- Scrapes business listings from **Google Maps**
- Extracts **name**, **phone number**, **address**, **Plus Code**, and **website**
- Saves results directly to a **Google Sheet**
- Reads city or business queries dynamically from another sheet
- Automatically resumes for multiple queries
- Prevents duplicate entries with tracking
- Detects and skips unavailable or malformed listings

---

## Project Structure
Google-Map-Scraper/
<br>│
<br>├── main.py # Main scraper script
<br>├── requirements.txt # Python dependencies
<br>├── README.md # Project documentation
<br>└── credentials.json # Google API credentials (Service Account)


---

## Prerequisites

Before running the script, ensure you have:

- Python **3.8+**
- **Google Cloud Service Account** with Sheets and Drive API enabled  
- **Google Chrome** browser installed  
- **ChromeDriver** (must match your Chrome version)  
- Access to a Google Sheet named:  
  > `Google Map Scraping (Python)`  
  with two sheets:  
  - **City** → contains search queries  
  - **Data** → where results will be stored  

---

## Installation & Setup


### 1️⃣ Clone the repository
```bash
git clone https://github.com/monojitbgit/google-map-scraper.git
cd google-map-scraper
```


### 2️⃣ Install dependencies

pip install -r requirements.txt



### 3️⃣ Create and connect your Google credentials

Go to Google Cloud Console.
<br>Create or use an existing Service Account.
<br>Enable:
<br>Google Sheets API
<br>Google Drive API
<br>Download the JSON key file.
<br>Rename it to credentials.json and place it in your project folder.
<br>Share your Google Sheet with the Service Account found inside credentials.json):
> `your-service-account@your-project.iam.gserviceaccount.com`


### 4️⃣ Verify ChromeDriver setup

Download ChromeDriver matching your installed Chrome version from:
<br>https://chromedriver.chromium.org/downloads
<br>Add it to your system PATH or keep it in the project folder.

---

<br>

## Running the Scraper

Once everything is configured, simply run:
<br>python gmapscraper.py

The script will:
<br>Authenticate with Google Sheets
<br>Read queries from the City sheet (Column A)
<br>For each query, open Google Maps
<br>Extract all available business details
<br>Write results to the Scraping sheet
<br>Mark the query status in the City sheet

---

## Dependencies

Listed in requirements.txt:
<br>selenium
<br>gspread
<br>google-auth
<br>beautifulsoup4

Install them all:
<br>pip install -r requirements.txt

---
## License

This project is licensed under the MIT License.
<br>You’re free to use, modify, and distribute it with attribution.
