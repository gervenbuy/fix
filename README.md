# 電車男 維修中心

這個 repo 有兩部分：

| 路徑 | 用途 | 對象 |
|---|---|---|
| `index.html` | 線上維修單（客戶填寫，資料送到 Google Sheet） | 客戶 |
| `notes/` | 維修筆記與 SOP，讓夥伴查閱、傳承 | 團隊夥伴 |

## 維修筆記結構

```
notes/
├── index.html                 ← 筆記目錄（所有筆記從這裡連過去）
├── _template/note.html        ← 新筆記範本
└── <車型>/<主題>.html          ← 每篇筆記，例如 t1-t3/meter-settings.html
```

目前收錄：

- **T1 / T3 頂配版 儀表後台參數設定手冊** — `notes/t1-t3/meter-settings.html`
  （原本放在 `gervenbuy/t3-setting`，已整合進來）
- **36V 外掛電池包 規格** — `notes/parts/36v-battery-pack.html`

## 新增一篇筆記

1. 在 `notes/` 底下建立車型資料夾（英文小寫、用 `-` 連接，例如 `ninebot-max`）。
2. 複製 `notes/_template/note.html` 到該資料夾，改成主題名稱（例如 `throttle-calibration.html`）。
3. 修改標題與內容；`note` 是補充說明框，`warn` 是注意事項框。
4. 到 `notes/index.html` 加一張卡片連到新筆記。
