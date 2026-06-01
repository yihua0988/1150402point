<div align="center">

# 🚧 AIoT 主動式工安防護系統
**Next-Generation Smart Construction Safety System**

從「被動通報」邁向「實體防禦」的工業級 AI 解決方案

[![Status](https://img.shields.io/badge/Project_Status-Active-10b981?style=for-the-badge&logo=checkmarx)](https://github.com/yihua0988/1150402point)
[![Architecture](https://img.shields.io/badge/Architecture-Edge_Computing-0ea5e9?style=for-the-badge&logo=serverless)](https://github.com/yihua0988/1150402point)
[![AI Model](https://img.shields.io/badge/AI_Model-YOLO_Vision-f59e0b?style=for-the-badge&logo=opencv)](https://github.com/yihua0988/1150402point)
[![Protocol](https://img.shields.io/badge/Protocol-MQTT_IoT-ef4444?style=for-the-badge&logo=mqtt)](https://github.com/yihua0988/1150402point)

[系統展示與架構簡報 (Live Demo) ](https://yihua0988.github.io/1150402point/)

</div>

---

## 💡 專案願景 (Project Vision)

> **「工安意外往往發生在一瞬間，光靠手機推播通知，根本來不及阻止遺憾發生。」**

本專案源自於第 21 屆育秀盃數位應用類獲獎作品的實務延伸。我們發現，傳統的智慧工地系統過度依賴「雲端運算」與「事後通知」，導致反應時間過長。

因此，次世代架構的升級目標非常明確：**打造一套不依賴外部網路、在現場就能完成 AI 判斷，並具備「實體機電阻斷能力」的主動式防護網。** 用軟體作為大腦，用硬體作為手腳，將被動的「事後檢討」轉變為主動的「事前防禦」。

---

## 核心概念 (Core Concepts)

### 🧠 1. 邊緣運算與封閉網路 (Edge-First Architecture)
捨棄容易產生延遲的雲端架構，將算力直接扎根於工地現場。
* **機動感測：** 採用 IP67 級 Wi-Fi CCTV，支援行動電源獨立供電，免除複雜拉線工程。
* **現場大腦：** 搭載 GPU 效能的現場工業主機被封裝於防水弱電箱內，在現場瞬間完成 YOLO 影像辨識與 NVR 錄影。
* **頻寬優化：** 系統僅分配 50MB 固定頻寬將畫面同步至中控室，將最核心的效能與頻寬留在現場進行即時防護。

### ⚡ 2. 實體連動與主動嚇阻 (Active Physical Defense)
不再只是發送 LINE 訊息，而是直接啟動現場防護。
* **極速反應：** 當 AI 判定違規（如未戴安全帽、誤闖危險區），系統在 **0.5 秒內**透過 MQTT 協定驅動現場繼電器 (Relay)。
* **實體警報：** 瞬間觸發高分貝閃光警鈴，第一時間嚇阻危險動作，大幅降低職災或火災風險。

### 🛡️ 3. 工業級資安與雙重解除 (Industrial Security & Dual Acknowledge)
防護機制的嚴謹度，決定了系統的可靠性。
* **雙重解除機制：** 現場按下實體按鈕僅能「暫停」警鈴，系統狀態仍會被鎖定。必須由中控室主管確認畫面無誤後，才能從後台徹底解除，嚴防現場人員盲目關閉警報。
* **單向調閱原則：** 遠端手機 APP 僅限調閱中控室的「備份紀錄」，無法直接對現場大腦進行設定修改，確保核心運算資源不被外部連線拖垮，並達到最高層級的資安防護。

---

## 📊 商業落地與可行性 (Commercial Feasibility)

本系統具備高度的商業轉化潛力與務實的建置規劃：

| 評估維度 | 實作策略 | 核心優勢 |
| :--- | :--- | :--- |
| **開源免月費** | 軟體層全數採用開源框架建置 | 企業無需負擔持續性的高昂軟體訂閱費 |
| **精準預算** | 資源傾斜於 GPU 邊緣主機與網路骨幹 | 整套硬體建置成本控制於 **NT$ 300,000** 內 |
| **高移植性** | 模組化硬體設計與無線終端配置 | 建案完工後，整套設備可**直接移轉至下一工地** |
| **穩健時程** | 12 週標準開發期 (含 5~9 週 AI 模型調校) | 保留充分壓力測試時間，系統上線即具備實戰力 |

---

## 🛠️ 技術堆疊 (Tech Stack)

* **AI 影像辨識:** `YOLO` / `Computer Vision`
* **物聯網通訊:** `MQTT` / `Wi-Fi CCTV`
* **邊緣運算:** `GPU Edge Server` / `Python`
* **機電控制:** `GPIO` / `Relay Module` / `Dual Acknowledge Logic`
* **前端展示:** `HTML5` / `CSS3 (Glassmorphism)` / `JavaScript`

---

<div align="center">
  <p><i>「用科技，保護每一個在現場流汗的生命。」</i></p>
  <b>Design & Planned by 洪益華 (Yi-Hua Hung)</b><br>
  <sup>Department of Information Technology, O.C.U.</sup>
</div>