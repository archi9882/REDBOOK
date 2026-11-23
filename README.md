# 紅筆英文本

個人英語學習筆記本。黑筆寫原本的說法，紅筆寫更道地的說法；另有片語庫、單字庫（冷僻字、詞源與字首字根標籤）、間隔複習與寫作練習。

> **這是私人 repo**：內含個人學習資料，請勿改成公開。

## 目錄

| 路徑 | 內容 |
|---|---|
| `app/red-pen-notebook.html` | 原版網頁（單一 HTML 檔），取自已發布的 artifact，版本 `1795400054-c4a1` |
| `app/red-pen-notebook-grimoire.html` | 魔導書版（副本，另含第二個 `<script>`），版本 `1795447220-cd77` |
| `docs/` | 專案文件：魔導書繼承文件、IELTS 紅筆筆記本與其魔法世界副本 |
| `data/` | 資料庫匯出（見下方說明） |

## 兩個網頁的來源

- 原版：<https://claude.ai/artifact/B5TVBUfN5jWHZudUXRwN8b>（slug `519aaf26-5c9d-4ffe-988f-5052ed327b1c`）
- 魔導書版：<https://claude.ai/artifact/BWtrYz5HQTNzmGYvnF45y8>（slug `5527e98c-751f-44bd-bce7-bf119a79d77f`）

兩個頁面是單檔 HTML。**在 Claude 裡執行時**，資料同步到該 artifact 的資料庫（`state/u`、`etym`、`phr`、`rec`、`pending`、`col`）。**單獨在瀏覽器開啟時**沒有資料庫，進度只存在瀏覽器的 localStorage（鍵名以 `rp-` 開頭），也不會有每晚的自動補貨與核對。

## 注意

- 原版 `red-pen-notebook.html` 是正式使用中的版本，修改請先在副本上試。
- 資料庫的詞源庫（`etym`）有些條目是已核對來源的（`rv: 2`），有些還在待核對。

## data/ 目錄（你自己的學習資料）

| 檔案 | 內容 |
|---|---|
| `words-1/2/3.jsonl` | 單字本內容（每行一個單字，精簡欄位；已略去內部時間戳與核對旗標） |
| `phr.jsonl` | 片語庫（內建、推薦、自訂，精簡欄位） |
| `custom-phrases.json` | 你自行輸入的 60 條片語 |
| `col.json` | 已收集單字清單（170 個，單字 → 收集日期） |
| `pending.json` | 待核對單字（單字 → 輸入日期） |
| `srs-state.json` | 複習進度、待用單字托盤 |

> 這是 2026-11-23 的快照，不會自動同步；artifact 資料庫仍是資料來源。
> 未收錄：`etym` 詞條庫、`rec`、AI 補充說明（`pai`）、每日備份（`state/bak-*`）、標註與分類（`cls`）。
