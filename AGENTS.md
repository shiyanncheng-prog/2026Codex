# 個人化 Agent 專案設定

我的工作是臨床醫師、教研部主任與醫務秘書，日常作業包含病人診療、臨床教學與醫務管理。我以前用 AI 工具最困擾的是回答沒來源依據。

我希望我的 Agent 個人化提示可以：
1. 語氣親切。
2. 呈現方式專業，依據實證醫學回答並引用來源。
3. 扮演臨床醫師、醫學專家與醫院管理專家的角色。
4. 仔細思考，推理合乎邏輯。
5. 產出前若資訊不足，先詢問我 3-5 個關鍵問題，幫助了解需求後再設計提示。
6. 最後將需求轉化為明確條件，並用 `Clear / Role / Constraints / Schemas / Reverse` 五段標題輸出。

---

# 教學駕駛艙 - AGENTS.md

## 專案入口

專案名稱：教學駕駛艙
專案用途：用於臨床教學的教學駕駛艙與相關工具工作區。
主要工作目錄：G:\我的雲端硬碟\2026Codex
GitHub repo：https://github.com/shiyanncheng-prog/2026Codex
GitHub Pages：https://shiyanncheng-prog.github.io/2026Codex/
預設 branch：main

## Obsidian 對應筆記

Obsidian vault：G:\我的雲端硬碟\Secondbrain
專案駕駛艙：教學駕駛艙\專案工作流程.md
收工時優先更新：同上

> 注意：專案駕駛艙是 Obsidian vault 裡的一篇筆記，不是工作資料夾裡的 Markdown 檔。

## 工作桌 + 三個家

- 工作桌：G:\我的雲端硬碟\2026Codex
- GitHub：https://github.com/shiyanncheng-prog/2026Codex
- Obsidian：G:\我的雲端硬碟\Secondbrain + 教學駕駛艙\專案工作流程.md
- Firebase：目前 repo 內已有 `.firebaserc`、`firebase.json`、`firestore.rules`；實際 project id 以 `.firebaserc` 為準。

## 同步規則

開工時：
- 使用 `startup-sync` 流程；若 skill 尚未安裝，手動讀本檔、讀 Obsidian 駕駛艙、檢查 Git 狀態。
- 不自動 pull / commit / push。

收工時：
- 使用 `shutdown-sync` 流程；若 skill 尚未安裝，手動盤點本次工作、更新 Obsidian 駕駛艙、檢查 Git diff。
- 如規則、路徑、專案邊界改變才更新本檔。
- 需要時才 commit + push GitHub，且只納入本次相關檔案。

新專案初始化時：
- 使用 `project-init-sync` 流程；若 skill 尚未安裝，依 #07 懶人包先盤點現況，只補缺口，不覆蓋既有設定。

## 主要檔案

入口檔：gemini-api-test.html
設定檔：firebase.json、firestore.rules、.firebaserc
部署位置：GitHub Pages，main branch 根目錄
專案說明：README.md

## 不要做

- 不要把每日進度寫進 AGENTS.md。
- 不要自動納入無關 git 變更。
- 不要把 API key、token、密碼寫進 repo。
- 不要儲存學生姓名；正式資料只用座號與班級代號。
