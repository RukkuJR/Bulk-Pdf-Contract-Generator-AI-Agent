# N8N Bulk PDF Generator AI Agent 🤖📄

Automate bulk PDF generation from Google Sheets data using N8N. Perfect for contracts, invoices, certificates, and reports.

## 🎯 What It Does

This workflow automatically:
1. Reads data from Google Sheets
2. Creates personalized PDF documents for each row
3. Saves files to Google Drive
4. Sends notifications when complete

**Example:** Generate 100 personalized service agreements in minutes instead of hours.

## 🏗️ How It Works

```
Start → Read Google Sheet → Loop Through Rows → Copy Template → 
Fill Data → Download → Notify → Upload to Drive → Repeat
```
<img width="1603" height="247" alt="aa2" src="https://github.com/user-attachments/assets/405fe804-213d-457f-ba37-85f377fc6140" />

### The Flow

1. **Manual Trigger** - Start the workflow
2. **Get Rows** - Fetch data from Google Sheets
3. **Loop** - Process each row (3 at a time)
4. **Copy Template** - Duplicate your PDF template
5. **Update Document** - AI fills in the data
6. **Download & Upload** - Save to Google Drive
7. **Send Notification** - Alert when done

## 💼 Use Cases

- **Contracts**: Service agreements, NDAs, employment contracts
- **Invoices**: Automated billing for multiple clients
- **Certificates**: Course completions, awards
- **Reports**: Monthly performance, compliance docs
- **Proposals**: Sales quotes, project proposals

## 📦 What You Need

- N8N installed (cloud or self-hosted)
- Google account with Sheets & Drive
- PDF template
- Spreadsheet with your data

## 🚀 Quick Setup

### 1. Prepare Your Google Sheet
Create columns for your data:
```
Client Name | Date | Amount | Terms | etc.
```

### 2. Create PDF Template
- Make a Google Doc or PDF with placeholders like `{{client_name}}`
- Upload to Google Drive

### 3. Set Up N8N

**Import the workflow** into N8N

**Connect Google Sheets:**
- Add your Google credentials
- Select your spreadsheet

**Connect Google Drive:**
- Add your Google credentials
- Set template file location
- Choose output folder

**Test:**
- Run with 3-5 test rows first
- Check outputs in Drive

## ⚙️ Configuration

### Basic Settings
```javascript
SHEET_ID = "your-google-sheet-id"
TEMPLATE_ID = "your-template-file-id"
OUTPUT_FOLDER = "your-drive-folder-id"
BATCH_SIZE = 3  // Process 3 items at a time
```

### Map Your Fields
Tell N8N which data goes where:
```javascript
{{client_name}} → Column A
{{date}} → Column B
{{amount}} → Column C
```

## 🔧 Troubleshooting

**Can't read Google Sheet?**
- Check credentials and permissions
- Verify sheet ID

**Template not found?**
- Check file ID
- Verify sharing settings

**Upload failed?**
- Check Drive folder permissions
- Check storage quota

## 💡 Tips

- Start small (test with 5 rows)
- Adjust batch size based on your needs
- Use clear column names in your sheet
- Keep template formatting simple

## outpout
<img width="1428" height="728" alt="aa1" src="https://github.com/user-attachments/assets/410c79b8-baa7-46ed-9825-7e368b3aae25" />
