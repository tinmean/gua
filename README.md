# 文王六爻（納甲）靜態排盤

純靜態網站版本，無後端、無資料庫、無 build step。直接部署到 GitHub Pages 或任何靜態主機即可使用。

## 檔案結構

- `index.html`：主程式（含全部 CSS/JS）
- `data/hexagrams_zh_tw.json`：64 卦中文名稱與上下卦資訊
- `data/king_wen_mapping.json`：六爻 bits（bit0=初爻、1=陽）對應文王序卦 id
- `data/rules.json`：世應、卦身、六獸、納甲、五行六親、旬空、神煞規則

## GitHub Pages 部署

1. 建立 GitHub repo，將以上檔案推上 `main`（或 `docs/` 目錄也可）。
2. 進入 repo 設定 `Settings` → `Pages`。
3. `Build and deployment` 選 `Deploy from a branch`。
4. Branch 選 `main`，資料夾選 `/ (root)`，儲存。
5. 約 1~3 分鐘後，使用 Pages URL 開啟。

## 使用方式

1. 輸入時間（台北時區，`YYYY-MM-DD HH:mm`）。
2. 直接輸入六爻（下→上），或先用銅錢法每爻三枚後一鍵帶入。
3. 點 `排盤`。
4. 點 `下載盤面 PNG` 匯出卡片圖。
5. 可切換簡潔/詳細模式；列印時僅印盤面卡片。

## URL Hash 分享

狀態保存在 hash：`#lines=...&dt=...&mode=...&sb=...`

範例（請換成你的實際網域）：

- `#lines=7,8,9,6,7,8&dt=2026-02-16%2014:30&mode=detail&sb=day_branch`
- `#lines=6,6,7,9,8,7&dt=2025-01-03%2009:10&mode=simple&sb=day_branch`
- `#lines=9,8,8,7,6,9&dt=2024-08-08%2020:15&mode=detail&sb=year_branch`

## Dev 驗收面板

在網址加上 `?dev=1` 會顯示內建 5 組固定案例，用於人工核對：

- 本卦 id / 之卦 id
- 世爻 / 應爻
- 卦身爻位
- 旬空
- 六獸首位

