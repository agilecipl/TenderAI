TenderAI SaaS Demo
===================

This archive contains a simplified standalone version of the TenderAI platform you asked for. You can run it locally on your own computer without any programming knowledge.

What's inside:
--------------

- `tenderai_app/server.py`: A simple Python web server that lets you upload tender documents (PDF, DOCX, XLSX) and automatically extracts basic information like EMD, due date, and a short summary. It presents a clean dashboard and detail pages for each tender.
- `tenderai_app/app.py`: A Flask-based server (requires Flask) if you prefer to run with a framework.
- `tenderai_app/templates/` and `tenderai_app/static/`: HTML templates and CSS used by the server.
- `uploads/`: A folder where your uploaded documents will be stored.
- `tenders.json`: A JSON file where the application stores parsed tender data.

Prerequisites:
--------------

1. **Python 3.8 or later** installed on your machine.
2. **pdftotext** utility (part of `poppler-utils`) installed for PDF parsing. On Ubuntu/Debian you can install it with:

   ```sh
   sudo apt-get install poppler-utils
   ```

   On Windows, you can download Poppler from <https://blog.alivate.com.au/poppler-windows/> and add it to your PATH.

3. **openpyxl** library for reading Excel files. Install it using pip:

   ```sh
   pip install openpyxl
   ```

How to run:
-----------

1. Extract `TenderAI_product.zip` to a folder.
2. Open a terminal/command prompt and navigate to the `tenderai_app` directory:

   ```sh
   cd tenderai_app
   ```

3. Start the server with Python:

   ```sh
   python server.py
   ```

   This will start the TenderAI server on port **8000**.

4. Open your web browser and go to:

   ```
   http://localhost:8000
   ```

5. You should see the TenderAI dashboard. Use the **Upload Tender Documents** form to select and upload your tender files. After upload, the dashboard will list each tender with extracted EMD, due date, and a short summary. Click **View** to see detailed information and the full text.

Enjoy testing your TenderAI platform!
