# 班級網站 - 老師部署指南

## 📁 檔案說明

```
class-website/
├── index.html    # 網站主檔案（勿修改）
├── data.json     # 資料設定檔（由老師編輯）
└── README.md     # 本說明檔
```

## ⚙️ 如何修改資料

編輯 `data.json` 檔案即可更新網站內容：

### 1. 班級基本資料
```json
"school": {
  "name": "○○國中一年甲班",  // 班級名稱
  "year": 115                // 學年度
}
```

### 2. 公佈欄
```json
"announcements": [
  {
    "date": "2026-03-05",      // 日期
    "title": "🎉 公告標題",     // 標題（可加 Emoji）
    "content": "公告內容..."    // 內文
  }
]
```

### 3. 每日作業
```json
"homework": [
  {
    "date": "2026-03-05",      // 作業日期
    "subject": "國語",          // 科目
    "content": "作業內容",      // 內容
    "due": "2026-03-06"        // 繳交期限
  }
]
```

### 4. 功課表
```json
"schedule": {
  "monday": ["國語", "數學", "英文", "自然", "社會", "綜合"],
  "tuesday": ["數學", "國語", "自然", "數學", "藝文", "體育"],
  "wednesday": ["英文", "社會", "國語", "數學", "自然", "綜合"],
  "thursday": ["國語", "英文", "數學", "社會", "體育", "自然"],
  "friday": ["數學", "綜合", "國語", "英文", "社會", "藝文"]
}
```

### 5. 活動照片
```json
"albums": [
  {
    "title": "🎊 活動名稱",           // 相簿標題
    "date": "2026-02-18",            // 活動日期
    "cover": "封面圖片網址",          // 列表顯示的封面
    "photos": [                      // 相簿內所有照片
      "圖片1網址",
      "圖片2網址"
    ]
  }
]
```

## 🖼️ 圖片網址怎麼取得？

### 方法一：使用 Google 雲端硬碟
1. 將圖片上傳到 Google 雲端硬碟
2. 對圖片按右鍵 → 共用 → 開放知道連結的人檢視
3. 複製連結，將 `view?usp=sharing` 改為 `uc?id=` + 檔案 ID
4. 或使用 https://imgbb.com 等圖床服務

### 方法二：使用圖床服務
- https://imgbb.com (免費)
- https://imgur.com (免費)
- 直接使用網路上的圖片網址

## 🚀 如何部署（免費）

### 方法一：GitHub Pages（推薦）

1. 註冊 GitHub 帳號
2. 建立新 Repository（名稱如 `class-website`）
3. 上傳 `index.html` 和 `data.json`
4. 進入 Settings → Pages
5. Source 選擇 `main branch`
6. 取得網址，如：`https://你的帳號.github.io/class-website/`

### 方法二：Vercel

1. 註冊 Vercel 帳號
2. 將 Repository 連接到 Vercel
3. 自動部署完成

### 方法三：Google 雲端硬碟 + HTML Viewer

1. 將資料夾設為公開
2. 使用 https://r.jina.ai/http://你的檔案網址 轉換
3. 或使用 HTML Viewer 之類的 APP

## 💡 快速更新小技巧

### VS Code（推薦）
- 安裝 VS Code
- 安裝「Live Server」擴充功能
- 右鍵 index.html → Open with Live Server
- 編輯 data.json 後重新整理即可預覽

### 使用 Replit
1. 到 replit.com 建立新專案
2. 選擇「Static Website」
3. 上傳檔案即可線上預覽

## 🎨 自訂顏色（如需要）

在 index.html 的 `<style>` 中找到 `:root` 區塊：

```css
:root {
  --primary: #4A90D9;      /* 主色 */
  --secondary: #FF9F43;    /* 次色 */
  --danger: #FC5C65;       /* 警示色 */
}
```

修改顏色代碼即可改變網站配色。

## ❓ 常見問題

**Q: 作業太多放不下？**
A: 系統會自動依日期排序，顯示所有作業

**Q: 功課表要怎麼改？**
A: 直接修改 data.json 中 schedule 的內容

**Q: 照片怎麼加那麼多？**
A: 在 photos 陣列中持續新增網址即可

**Q: 網站會自動更新嗎？**
A: 是的！只要修改 data.json，儲存後重新整理網頁就會更新

## 📞 取得協助

如有問題，請聯繫網站管理員。
