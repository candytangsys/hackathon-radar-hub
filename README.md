# 黑客松雷達 Hub

一個持續更新的「線上可參加、有獎金的黑客松與競賽」知識庫網站。資料與版面分離：新增一筆活動只要在 `data/items.json` 加一個物件，`radar.html` 會自動渲染、排序、套用現有樣式。

- 網頁：<https://candytangsys.github.io/hackathon-radar-hub/>
- 專案規則（給 AI 助理看）：[`CLAUDE.md`](./CLAUDE.md)
- 規則摘要（給人看）：[`guide.html`](https://candytangsys.github.io/hackathon-radar-hub/guide.html)

## 專案結構

```
index.html        首頁
radar.html        黑客松雷達（資料驅動的活動清單）
guide.html        規則摘要頁
CLAUDE.md         給 AI 助理的完整專案規則
assets/style.css  全站共用樣式
data/items.json   所有已核實活動的結構化資料
entries/          （預留）單一活動的長篇介紹頁
```

## 本地預覽

這是純靜態網站，直接用任何靜態伺服器打開即可，例如：

```bash
cd hackathon-radar-hub
python3 -m http.server 8000
# 開啟 http://localhost:8000
```

## 如何新增一筆活動

1. 用官方頁面核實：是否線上可完整參加、有無現金或明確獎項、截止日是否已過。
2. 依 `CLAUDE.md` 第 4 節的欄位格式整理成一個物件，加進 `data/items.json`。
3. 確認 `radar.html` 能正確顯示新資料即可，不需要修改任何版面程式碼。

完整規則請見 [`CLAUDE.md`](./CLAUDE.md)。
