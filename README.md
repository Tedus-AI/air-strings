# Air Strings 空中弦

用雙手在空中拉出會發聲的弦，再用手指撥它。純網頁，不用安裝任何軟體。

**線上使用：** https://tedus-ai.github.io/air-strings/

## 怎麼玩

| 動作 | 做法 |
|---|---|
| 拉弦 | 雙手都用拇指捏住食指，往兩邊拉開再放開，弦就留在空中。單手捏住拖曳也可以。 |
| 撥弦 | 張開手，用食指或中指劃過弦。劃得越快聲音越大。 |
| 音高 | 弦越長音越低。預設自動對齊五聲音階，可改大調、小調、半音或自由音高。 |
| 刪除 | 點一下弦，按「✕ 刪除這條弦」；或用 ↶ 復原、「清空」。 |

沒有鏡頭時，可以按「只用觸控試玩」，用手指或滑鼠拉弦、撥弦。

## 建議裝置

- iPad / iPhone：用 Safari 打開，前鏡頭即可。iPad 立起來放、人離約 50～80 cm 效果最好。
- 電腦：需要網路攝影機，建議用 Chrome 或 Edge。

## 技術

- 手部追蹤：[MediaPipe Hand Landmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker)，在瀏覽器端執行，畫面不會上傳。
- 聲音：Web Audio，以 Karplus-Strong 演算法即時合成撥弦聲，含撥弦位置與音色參數。
- 部署：推到 `main` 後由 GitHub Actions 自動發布到 GitHub Pages，並自動蓋上版本號。

## 已知限制

- 光線太暗或背景很雜時，手部追蹤會不穩。
- 第一次開啟需要下載約 8 MB 的手部模型，之後會被瀏覽器快取。
