# 🫧 泡泡禪 Bubble Zen

一個沒有分數、沒有倒數、不會失敗的紓壓小遊戲。戳破飄浮的六角形泡泡，聽聽柔和的音階，需要時再跟著圓圈做幾次深呼吸。

純 HTML / CSS / JavaScript，**單一檔案、零依賴**，打開 `index.html` 就能玩。

## 玩法

| 操作 | 說明 |
| --- | --- |
| 點擊 / 輕觸 | 戳破泡泡 |
| 按住並滑過 | 一次戳破一整串 |
| 空白鍵 | 隨機戳破一顆（電腦） |
| 🔊 音效 | 開關聲音（泡泡越大音越低，使用五聲音階，怎麼戳都不會刺耳） |
| 🌬 呼吸 | 開啟呼吸引導：吸氣 4 秒、吐氣 6 秒 |
| 🎨 主題 | 切換 夜空 / 海洋 / 晨光 |

設定與累計數量會存在瀏覽器的 localStorage。若系統開啟「減少動態效果」，泡泡會自動放慢、不再搖晃。

## 在本機執行

直接用瀏覽器開啟 `index.html` 即可，或：

```bash
python3 -m http.server 8000
# 開啟 http://localhost:8000
```

## 上傳到 GitHub 並發佈成網頁

1. 在 GitHub 建立一個新的空儲存庫（例如 `bubble-zen`）。
2. 在本資料夾執行：

```bash
git init
git add .
git commit -m "Add Bubble Zen"
git branch -M main
git remote add origin https://github.com/<你的帳號>/bubble-zen.git
git push -u origin main
```

3. 到儲存庫的 **Settings → Pages**，Source 選 **Deploy from a branch**，Branch 選 `main` / `/ (root)`，儲存。
4. 約一分鐘後，就能在 `https://<你的帳號>.github.io/bubble-zen/` 玩到。

## 想自己改？

- 泡泡數量、速度、大小：`index.html` 內的 `spawn()` 與 `targetCount()`
- 新增主題：在 `THEMES` 陣列加一組背景與色相範圍
- 鼓勵小語：修改 `MESSAGES`
- 音階：修改 `SCALE`

## 授權

MIT License，詳見 [LICENSE](LICENSE)。
