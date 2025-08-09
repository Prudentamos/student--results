# Schools of Youngtec - Student Result Viewer

This is a clean, modern static website that allows parents and students to view and download student results securely by entering an Access Code. The results are fetched dynamically from a public Google Sheet via the Google Sheets API.

---

## Features

- Access Code input for secure lookup
- Fetches data from a public Google Sheet using API key
- Displays student results with PDF download links
- Responsive and modern UI using Bootstrap 5 and Feather icons

---

## Setup Instructions

1. **Google Sheet Setup**

   - Share your Google Sheet with **Anyone with the link (Viewer)** permission.
   - Note your **Spreadsheet ID** from the sheet URL.
   
2. **Google Cloud API Key**

   - Create a Google Cloud project.
   - Enable the **Google Sheets API**.
   - Create an **API Key** and restrict it to your website domain (optional but recommended).

3. **Configure the Website**

   - Open `index.html`.
   - Replace the placeholders with your actual values:
     ```js
     const API_KEY = 'YOUR_GOOGLE_SHEETS_API_KEY';
     const SPREADSHEET_ID = 'YOUR_SPREADSHEET_ID';
     const SHEET_NAME = 'Sheet1'; // or your sheet tab name
     ```
   - Replace the placeholder logo image (`logo-placeholder.png`) with your school logo (optional).

---

## Testing Locally

To test the website on your computer:

1. Open the `index.html` file in a modern web browser (Chrome, Firefox, Edge).
2. Enter an Access Code provided by the admin.
3. The site will fetch and display matching results from the Google Sheet.

> **Note:** For security reasons, some browsers block fetch requests from local files (`file://` protocol).  
> If you face issues, use a simple local server:

- **Python 3** (if installed):

  ```bash
  cd path/to/your/project
  python3 -m http.server 8000
