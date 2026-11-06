# 咖啡知識圖鑑｜The Coffee Index

以繁體中文介紹咖啡入門知識的雜誌風格網站。使用原生 HTML、CSS、JavaScript 與 JSON，可直接部署至 GitHub Pages。

## 專案功能
- 首頁：主視覺、搜尋、五大分類、本期選讀與網站介紹
- 分類瀏覽：依主題查看知識文章
- 搜尋：搜尋標題、摘要與內文
- 文章頁：導讀、分段內容、延伸閱讀與參考來源
- `AGENTS.md`：定義網站風格、內容格式、資料規則與 AI 維護流程

目前包含五大分類與十篇入門知識條目。

## 本機預覽
網站透過 JavaScript `fetch()` 讀取 JSON，請使用本機靜態伺服器預覽，不要直接雙擊 `index.html`。

在專案根目錄執行：

```bash
python -m http.server 8000
```

接著開啟 `http://localhost:8000`。

## 發布到 GitHub Pages
1. 在 GitHub 建立新的 Repository。
2. 將 ZIP 解壓縮後，進入 `coffee-encyclopedia` 資料夾。
3. 將資料夾內的所有檔案與資料夾上傳到 Repository 根目錄（不要多包一層資料夾）。
4. 進入 Repository 的 **Settings → Pages**。
5. Build and deployment 選擇 **Deploy from a branch**。
6. Branch 選擇 `main`，資料夾選擇 `/ (root)`，按 Save。
7. 等待 GitHub Pages 完成部署，再使用頁面顯示的網址瀏覽。

## 如何新增文章
先閱讀 `AGENTS.md`，依照文章欄位規範新增文章物件至 `data/articles.json`。新增前需查證資料、使用唯一 ID、選擇既有分類，並確認相關文章 ID 有效。

## 檔案結構

```text
coffee-encyclopedia/
├── AGENTS.md
├── README.md
├── index.html
├── .nojekyll
├── css/
│   └── style.css
├── js/
│   └── app.js
├── data/
│   ├── categories.json
│   └── articles.json
└── assets/
    └── favicon.svg
```

## 資料與著作權說明
網站文章為入門知識整理與重新撰寫，並提供延伸查閱來源。資料可能隨研究與業界用法更新，請以來源機構最新資訊為準。網站主視覺使用 CSS 原創插畫，不依賴未授權咖啡照片。
