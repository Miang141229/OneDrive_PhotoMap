# **OneDrive Photo Map 🗺️**

A serverless, single-page application that visualizes your OneDrive photos on an interactive map using their GPS data.

## **✨ Features**

* **🔒 Privacy First**: Runs entirely in your browser. No photo data is sent to any third-party server.  
* **🌍 Interactive Map**: Full-screen map powered by Leaflet and OpenStreetMap.  
* **⚡ Fast & Cached**: Scanned photo metadata is cached locally in your browser for instant loading next time.  
* **📱 Responsive**: Works great on desktop and mobile browsers.  
* **📍 Cluster View**: Automatically groups photos taken at the same location (Spiderfy effect).

## **🚀 Getting Started**

### **Prerequisites**

To use this app, you need a **Microsoft Azure Client ID**. This authorizes the app to read your OneDrive files.

1. Go to [Azure Portal \- App Registrations](https://www.google.com/search?q=https://portal.azure.com/%23view/Microsoft_AAD_RegisteredApps/ApplicationsListBlade).  
2. Click **New registration**.  
3. **Name**: Enter a name (e.g., OneDriveMap).  
4. **Supported account types**: Select **"Accounts in any organizational directory and personal Microsoft accounts"**.  
5. **Redirect URI**:  
   * Platform: Select **Single-page application (SPA)**.  
   * URI: Enter your local server URL, e.g., http://localhost:5500/index.html.  
6. Click **Register**.  
7. Copy the **Application (client) ID**.

### **Installation & Run**

1. Clone this repository or download the index.html file.  
2. Start a local web server (required for OAuth authentication).  
   * **VS Code**: Install "Live Server" extension \-\> Right-click index.html \-\> "Open with Live Server".  
   * **Python**: Run python \-m http.server 5500 in the terminal.  
3. Open the URL in your browser (e.g., http://localhost:5500/index.html).  
4. Paste your **Client ID** into the input box and click **Initialize**.  
5. Login with your Microsoft account and enjoy\!

## **🛠️ Technologies**

* [Microsoft Graph API](https://developer.microsoft.com/en-us/graph) \- For accessing OneDrive photos.  
* [MSAL.js](https://github.com/AzureAD/microsoft-authentication-library-for-js) \- For secure authentication.  
* [Leaflet.js](https://leafletjs.com/) \- For maps.  
* [Leaflet.markercluster](https://github.com/Leaflet/Leaflet.markercluster) \- For handling thousands of markers.  
* [Tailwind CSS](https://tailwindcss.com/) \- For styling.

## **⚠️ Notes**

* **Redirect URI Mismatch**: If you see an authentication error, ensure the URL in your browser matches *exactly* with the Redirect URI set in Azure Portal (including http vs https, localhost vs 127.0.0.1, and the trailing /index.html).

## **📄 License**

MIT License

# **OneDrive 相片地圖 🗺️**

這是一個無需後端伺服器的單頁應用程式 (SPA)，它能讀取您 OneDrive 照片中的 GPS 資訊，並將其呈現在互動式地圖上。

## **✨ 功能特色**

* **🔒 隱私優先**：完全在瀏覽器端執行，您的照片資料不會傳送至任何第三方伺服器。  
* **🌍 互動地圖**：基於 Leaflet 與 OpenStreetMap 的全螢幕地圖體驗。  
* **⚡ 快速且具備快取**：掃描過的照片資訊會儲存在瀏覽器快取中，下次開啟時可瞬間載入。  
* **📱 響應式設計**：在電腦與手機瀏覽器上皆可完美運作。  
* **📍 聚合檢視**：自動聚合同一地點拍攝的照片，點擊後會如蜘蛛網般散開方便檢視。

## **🚀 如何開始**

### **事前準備**

要使用此應用程式，您需要一組 **Microsoft Azure Client ID**，這用於授權應用程式讀取您的 OneDrive 檔案。

1. 前往 [Azure Portal \- 應用程式註冊](https://www.google.com/search?q=https://portal.azure.com/%23view/Microsoft_AAD_RegisteredApps/ApplicationsListBlade)。  
2. 點擊 **新註冊**。  
3. **名稱**：輸入任意名稱 (例如 OneDriveMap)。  
4. **支援的帳戶類型**：選擇 **「任何組織目錄中的帳戶和個人 Microsoft 帳戶」**。  
5. **重新導向 URI**：  
   * 平台：選擇 **單頁應用程式 (SPA)**。  
   * 網址：輸入您的本機伺服器網址，例如 http://localhost:5500/index.html。  
6. 點擊 **註冊**。  
7. 複製 **應用程式 (用戶端) 識別碼**。

### **安裝與執行**

1. 複製此專案或下載 index.html 檔案。  
2. 啟動一個本機網頁伺服器 (OAuth 驗證需要)。  
   * **VS Code**: 安裝 "Live Server" 套件 \-\> 右鍵點擊 index.html \-\> 選擇 "Open with Live Server"。  
   * **Python**: 在終端機執行 python \-m http.server 5500。  
3. 在瀏覽器開啟網址 (例如 http://localhost:5500/index.html)。  
4. 將您的 **Client ID** 貼入輸入框並點擊 **初始化**。  
5. 登入您的 Microsoft 帳號並開始使用！

## **🛠️ 使用技術**

* [Microsoft Graph API](https://developer.microsoft.com/en-us/graph) \- 讀取 OneDrive 相片。  
* [MSAL.js](https://github.com/AzureAD/microsoft-authentication-library-for-js) \- 安全驗證機制。  
* [Leaflet.js](https://leafletjs.com/) \- 地圖核心。  
* [Leaflet.markercluster](https://github.com/Leaflet/Leaflet.markercluster) \- 處理大量地圖標記。  
* [Tailwind CSS](https://tailwindcss.com/) \- 介面樣式。

## **⚠️ 注意事項**

* **重新導向 URI 不符**：如果出現驗證錯誤，請確保瀏覽器上的網址與 Azure Portal 設定的完全一致 (包含 http、localhost 以及結尾的 /index.html)。

## **📄 授權條款**

MIT License
