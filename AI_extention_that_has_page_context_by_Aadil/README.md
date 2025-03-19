# Browser Buddy with Webpage Context

## Project Structure

```
browser_buddy/
│
├── main.py                    # Main application entry point
├── webpage_context.py         # HTML content extraction and processing
├── browser_extension.py       # Socket server for browser extension communication
│
└── extension/                 # Browser extension files (for Chrome/Edge)
    ├── manifest.json          # Extension configuration
    ├── popup.html             # Extension popup interface
    ├── popup.js               # Extension popup logic
    ├── content.js             # Page content extraction script
    └── background.js          # Background service worker
    └── icons/                 # Extension icons
```

## Setup Instructions

### 1. Install Python Dependencies

```
pip install beautifulsoup4 selenium webdriver-manager requests
```

### 2. Install the Browser Extension

1. Open Chrome or Edge and navigate to `chrome://extensions` or `edge://extensions`
2. Enable "Developer mode" (toggle in the top right)
3. Click "Load unpacked" and select the `extension` folder from this project
4. The Browser Buddy extension should now be visible in your browser toolbar

### 3. Using Webpage Context

1. Start the Browser Buddy application
2. Navigate to the webpage you want to analyze
3. Click the Browser Buddy extension icon in your toolbar
4. Click "Send Page Content"
5. Now when you interact with Browser Buddy, it will have context about the current webpage

## How It Works

The browser extension captures the HTML content of the current webpage and sends it to the Browser Buddy application. The application processes this content to extract meaningful context, which is then included in your interactions with the AI assistant.

![Screenshot 2025-03-15 201405](https://github.com/user-attachments/assets/d074499d-8715-42f3-b8b3-1895e9995e80)

press reset to start a new chat

