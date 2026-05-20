# 團隊資源庫 PWA — 部署說明

## 📁 檔案結構
```
pwa-app/
├── index.html       ← 主程式（整個 app）
├── manifest.json    ← PWA 設定
├── sw.js            ← Service Worker（離線快取）
└── icons/
    ├── icon-192.png ← App 圖示（需自行準備）
    └── icon-512.png ← App 圖示（需自行準備）
```

---

## 🖼️ 準備圖示（必要）

需要兩個 PNG 圖示：
- `icons/icon-192.png`（192×192 px）
- `icons/icon-512.png`（512×512 px）

免費工具：https://favicon.io（可以用 emoji 或文字生成）

---

## 🚀 部署到 Vercel（免費，最簡單）

1. 註冊 https://vercel.com（免費）
2. 安裝 Vercel CLI：
   ```bash
   npm install -g vercel
   ```
3. 進入 pwa-app 資料夾，執行：
   ```bash
   vercel
   ```
4. 跟著提示操作，完成後會給你一個網址（例如 `https://team-resources.vercel.app`）

---

## 🚀 部署到 Netlify（免費，拖拉即可）

1. 開啟 https://app.netlify.com/drop
2. 把整個 `pwa-app` 資料夾**直接拖進去**
3. 幾秒鐘後取得網址，完成！

---

## 📱 手機安裝方式

### Android（Chrome）
1. 開啟網址
2. 點右上角選單 `⋮`
3. 選「加入主畫面」
4. 確認安裝

### iPhone（Safari）
1. 用 Safari 開啟網址（不能用 Chrome）
2. 點下方分享按鈕 `⬆`
3. 選「加入主畫面」
4. 點「新增」

---

## ✅ 功能說明

- **資料儲存**：用 localStorage，資料存在裝置本機
- **離線使用**：Service Worker 快取，沒有網路也能開啟
- **全螢幕**：安裝後無瀏覽器 UI，就像原生 app
- **手機適配**：支援安全區域（瀏海/Home Bar）

---

## 💡 進階選項

如果要讓**多人共用同一份資料**，需要加後端（如 Firebase、Supabase），
可以再告訴 Claude 幫你整合。
