# ¡Vamos! 拉美西語特訓營 🔥

A mobile-first web app (PWA) that drills **Latin American Spanish** using the FSI
Pattern-Drill method, for a zero-beginner. 中文＋English 講解。

一個手機優先的網頁 App，用 FSI Pattern Drill 高強度訓練拉丁美洲西班牙語。

---

## 🧠 學習法 / The method (built in)

| 步驟 | 名稱 | 做什麼 |
|---|---|---|
| ① | **回音法 Echo** | 聽母語發音＋音標，跟讀，建立耳朵與口腔記憶 |
| ② | **替換練習 Substitution** | 看提示詞，**3 秒內**說出完整句子；超時→「太慢了！」並重複 |
| ③ | **影子練習 Shadowing** | 每 5 次，跟讀一段流暢語音（含節奏標記），模仿母語節奏 |
| ④ | **情境輸出 Output** | 滿 20 次，給真實情境即興造句，附參考答案 |
| ♻️ | **間隔複習 SRS** | 新練習中隨機穿插「上一組」舊提示詞，鞏固長期記憶（Leitner 1–5 盒） |

語塊 (Chunking)：每課一個高頻核心句型，例如 `Quiero ___ , por favor.`

目前 6 課：`Quiero` / `¿Dónde está?` / `¿Cuánto cuesta?` / `Me gustaría` /
`¿Puedo...?` / `Necesito`，涵蓋旅遊・商務・日常。

---

## 📱 怎麼放到手機上 / Get it on your phone

App 是純前端、無後端，進度存在手機 localStorage，發音用瀏覽器內建語音（Web Speech）。

### 選項 A：免費靜態託管（最推薦，可離線安裝、發音最完整）
任選一個免費平台，把整個資料夾傳上去，得到一個 https 網址，手機打開即可：

- **Netlify Drop** — 最簡單，免帳號：開 <https://app.netlify.com/drop>，把 `D:\nuad` 整個資料夾拖進去，幾秒後得到網址。
- **GitHub Pages** — 若你有 GitHub：把資料夾推到一個 repo，Settings → Pages → 部署 `main` 分支根目錄。
- **Vercel / Cloudflare Pages** — 拖資料夾或連 repo 即可。

> 拿到 https 網址後，在手機瀏覽器打開 → 分享選單 →「加入主畫面 / Add to Home Screen」，
> 就會像 App 一樣全螢幕、可離線使用。

### 選項 B：同一個 Wi-Fi 區網（馬上試）
此電腦正在跑伺服器。手機連到**同一個 Wi-Fi**，瀏覽器打開：

```
http://192.168.50.225:5173
```

（若打不開：Windows 防火牆可能擋了 5173 連接埠；用選項 A 最穩。）

### 選項 C：直接傳檔案
把 `index.html` 用 email / 雲端傳到手機，用瀏覽器開啟也能練（發音可用；
但「加入主畫面」與離線快取需要選項 A 的 https）。

---

## 🔊 關於發音 / About the voice

- 發音由**手機內建的西語語音**提供（iPhone、Android 都內建 es-MX / es-US）。
- 開 ⚙️ 設定可挑聲音、調語速；建議選 **es-MX** 或 **es-US** 最自然。
- 第一次播放請先點一下按鈕（手機需要使用者互動才會解鎖語音）。
- 「語音作答」（用說的自動評分）為實驗功能，需 Chrome／Android、麥克風權限與網路。

---

## 🖥️ 本機開發 / Run locally

```powershell
# 任一方式，於 D:\nuad 資料夾啟動靜態伺服器：
npx -y serve -l 5173 .
#   或
python -m http.server 5173
```

然後開 <http://localhost:5173>。

## 📂 檔案 / Files
- `index.html` — 整個 App（HTML＋CSS＋JS＋課程內容，單檔可攜）
- `manifest.webmanifest` — PWA 設定（加入主畫面）
- `sw.js` — Service Worker（離線快取）
- `.claude/launch.json` — 預覽伺服器設定

¡Mucho éxito! 💪
