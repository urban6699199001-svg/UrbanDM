# Urban OS 上線指南

## 📁 檔案清單

| 檔案 | 說明 |
|------|------|
| `insurance-calculator-v7.html` | 保險試算系統 v7.28（含 DM 按鈕） |
| `dm-designer.html` | DM 設計器 v2.0 |

**注意：兩個檔案必須放在同一資料夾！**

---

## 🚀 上線方案

### 方案一：GitHub Pages（推薦・免費）

1. **建立 GitHub 帳號**（如果還沒有）
   - https://github.com/signup

2. **建立新 Repository**
   - 點擊右上角 `+` → `New repository`
   - 名稱：`urban-os`（或你喜歡的名稱）
   - 勾選 `Public`
   - 點擊 `Create repository`

3. **上傳檔案**
   - 點擊 `uploading an existing file`
   - 拖曳 `insurance-calculator-v7.html` 和 `dm-designer.html`
   - 點擊 `Commit changes`

4. **啟用 GitHub Pages**
   - 進入 `Settings` → `Pages`
   - Source: `Deploy from a branch`
   - Branch: `main` → `/ (root)`
   - 點擊 `Save`

5. **等待 1-2 分鐘後，網址為：**
   ```
   https://你的用戶名.github.io/urban-os/insurance-calculator-v7.html
   https://你的用戶名.github.io/urban-os/dm-designer.html
   ```

---

### 方案二：Netlify（拖放上線・免費）

1. 到 https://app.netlify.com/drop
2. 把兩個 HTML 檔案打包成資料夾
3. 整個資料夾拖曳到網頁上
4. 立即獲得網址！

---

### 方案三：Firebase Hosting（你已有 Firebase）

1. **安裝 Firebase CLI**
   ```bash
   npm install -g firebase-tools
   ```

2. **登入並初始化**
   ```bash
   firebase login
   firebase init hosting
   ```
   - 選擇 `urban-os-v1` 專案
   - Public directory: `public`
   - Single-page app: `No`

3. **將檔案放入 public 資料夾**
   ```
   public/
   ├── insurance-calculator-v7.html
   └── dm-designer.html
   ```

4. **部署**
   ```bash
   firebase deploy --only hosting
   ```

5. **網址：**
   ```
   https://urban-os-v1.web.app/insurance-calculator-v7.html
   ```

---

## 🔗 使用流程

```
試算系統 → 輸入資料 → 試算結果 → 點擊「生成 DM」→ DM 設計器
```

DM 設計器會自動帶入：
- 商品代碼
- 方案（年期）
- 投保年齡
- 性別
- 保額
- 查詢年齡（預設 +30 歲）

---

## 💡 小提醒

1. **HTTPS**：Firebase/GitHub Pages/Netlify 都自動提供 HTTPS
2. **快取**：更新檔案後可能需要清除瀏覽器快取（Ctrl+Shift+R）
3. **手機**：這兩個頁面都支援手機瀏覽

---

## 🛠️ 如果需要自訂網域

GitHub Pages 和 Netlify 都支援自訂網域：
- `urban-os.yourdomain.com`

設定方式請參考各平台說明文件。
