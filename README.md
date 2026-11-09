# Gemini CoC TRPG 7版 自動化跑團引擎

這是一套基於 Gemini 打造的 8 模組 CoC 7 版跑團系統。將複雜的 KP 推進、機制檢定與角色追蹤分離，確保 AI 輸出的敘事自然生動，並嚴格遵循遊戲規則。

## 核心機制特色
* **嚴謹的角色防呆追蹤：** 角色卡採用 `總值% (基X+點Y+成Z)` 格式。系統設定了強制的防呆限制，未經玩家明確同意並確認 Markdown 草稿前，絕對禁止自動變更技能數值。
* **雙階段盲骰：** 將隨機性判定與數據計算徹底分離，避免 AI 產生常見的數值偏誤。
* **語言與溝通障礙檢定：** 依照母語與外語技能進行嚴格判定，若語言不通則轉為高難度說服或話術。
* **動態理智 (SAN) 判定：** 在敘事段落完成後無縫觸發，保持故事沉浸感。

## 系統架構 (8 大模組)
請至 `prompts/` 資料夾查看各技能的完整 Prompt 系統指令：
1. `coc-kp-system`: KP 推進主控台
2. `coc-mechanics-system`: 檢定與戰鬥結算核心
3. `coc-character-tracker`: 角色資料庫追蹤
4. `coc-story-formatter`: 敘事與選項輸出格式
5. `coc-session-memory`: 單次劇本暫時記憶
6. `coc-narrative-writer`: 第三人稱場景敘事
7. `coc-character-creator`: 角色/NPC 生成器
8. `coc-npc-designer`: 動態 NPC 心理與地雷設計
