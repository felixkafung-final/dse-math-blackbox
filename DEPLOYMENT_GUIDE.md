# 🚀 GitHub Pages 部署指南

## 完整步驟教學

### 第一步：在 GitHub 創建新倉庫

1. 打開瀏覽器，訪問 [https://github.com](https://github.com)
2. 登錄你的 GitHub 賬號（如果沒有賬號，需要先註冊）
3. 點擊右上角的 **+** 號，選擇 **New repository**
4. 填寫倉庫信息：
   - **Repository name**: `dse-math-blackbox`（建議名稱，你可以自定義）
   - **Description**: `DSE 數學算法黑盒 - 官方網站`
   - **Public**: 選擇 Public（公開）
   - **不要勾選** "Add a README file"（我們已經有了）
   - 點擊 **Create repository**

### 第二步：推送代碼到 GitHub

在你的電腦上，打開 PowerShell（當前已在項目文件夾），運行以下命令：

```powershell
# 1. 添加遠程倉庫（請替換 YOUR_USERNAME 為你的 GitHub 用戶名）
git remote add origin https://github.com/YOUR_USERNAME/dse-math-blackbox.git

# 2. 重命名分支為 main（GitHub 新標準）
git branch -M main

# 3. 推送代碼到 GitHub
git push -u origin main
```

**⚠️ 重要：** 記得將 `YOUR_USERNAME` 替換成你的 GitHub 用戶名！

例如，如果你的用戶名是 `felix_math`，命令應該是：
```powershell
git remote add origin https://github.com/felix_math/dse-math-blackbox.git
```

### 第三步：啟用 GitHub Pages

1. 推送成功後，回到 GitHub 網頁上的你的倉庫頁面
2. 點擊倉庫的 **Settings**（設置）標籤
3. 在左側菜單中找到並點擊 **Pages**
4. 在 "Source" 部分：
   - **Branch**: 選擇 `main`
   - **Folder**: 選擇 `/ (root)`
   - 點擊 **Save**

### 第四步：等待部署完成

1. GitHub 會開始自動部署你的網站
2. 等待 1-3 分鐘
3. 刷新頁面，你會看到一個綠色的提示框：
   ```
   Your site is live at https://YOUR_USERNAME.github.io/dse-math-blackbox/
   ```
4. 點擊這個鏈接，就能訪問你的網站了！

### 第五步：分享你的網站

你的網站地址格式：
```
https://YOUR_USERNAME.github.io/dse-math-blackbox/
```

**例子：**
- 如果用戶名是 `felix_math`
- 網址就是：`https://felix_math.github.io/dse-math-blackbox/`

---

## 📝 常見問題

### Q1: 推送代碼時要求輸入用戶名和密碼怎麼辦？

**A:** GitHub 不再支持密碼驗證，你需要使用 Personal Access Token：

1. 訪問 [https://github.com/settings/tokens](https://github.com/settings/tokens)
2. 點擊 **Generate new token** → **Generate new token (classic)**
3. 設置：
   - Note: `DSE Math BlackBox`
   - Expiration: `90 days` 或更長
   - 勾選 `repo` 權限
4. 點擊底部的 **Generate token**
5. **複製生成的 token**（只會顯示一次！）
6. 在推送時，用戶名輸入你的 GitHub 用戶名，密碼輸入剛才複製的 token

### Q2: 網站部署後顯示 404 錯誤？

**A:** 可能的原因：
1. 等待時間不夠，再等 2-3 分鐘
2. 檢查 Settings → Pages 中的 Branch 是否選擇正確
3. 確保 `index.html` 文件在倉庫根目錄

### Q3: 如何更新網站內容？

**A:** 修改文件後，運行：
```powershell
git add .
git commit -m "Update content"
git push
```
等待 1-2 分鐘，網站會自動更新。

### Q4: 可以使用自定義域名嗎？

**A:** 可以！在 Settings → Pages → Custom domain 中輸入你的域名，然後：
1. 在你的域名提供商處添加 CNAME 記錄
2. 指向 `YOUR_USERNAME.github.io`

---

## 🎉 完成後的下一步

1. **測試網站**：在不同設備（手機、電腦）上打開網站，確保顯示正常
2. **分享鏈接**：將網址分享到小紅書、抖音等平臺
3. **SEO 優化**：提交到 Google Search Console
4. **追蹤流量**：可以添加 Google Analytics

---

## 📞 需要幫助？

如果遇到任何問題，請：
1. 檢查 GitHub 倉庫的 Actions 標籤，查看部署日誌
2. 確保所有命令都正確執行
3. 確認 GitHub 用戶名拼寫無誤

---

**祝你成功部署！🎊**

© 2026 數學滿分匠 Felix
