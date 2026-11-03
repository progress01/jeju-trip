# 濟州島家族旅行（2026/12/15–12/20）

全家一起討論行程用的網頁。

## 怎麼用

- **總覽看板**：每天一欄，左右滑動。點卡片看細節，點日期看整天。
- **編輯模式**：打開後按住卡片左邊的點點拖曳，可以在不同天、不同方案（12/19 的 A／B／C）、口袋名單之間搬動。點卡片可以修改時間、說明、費用、地圖搜尋字，或用「放在」直接移到別天（手機上比拖曳方便）。
- **改完之後**有兩種做法：
  - **分享給家人看**：產生一個連結貼到 LINE。家人打開就看到你的版本，有變動的地方會標顏色（綠＝新增、藍＝移動、橘＝修改）。不會改到正式版本。
  - **存到 GitHub**：變成正式版本。需要這個 repo 的寫入 token（見下方）。
- **修改紀錄**：每次存到 GitHub 都會留一筆，可以看「這次改了什麼」，也能把舊版本叫出來接著改。

修改在發布之前只存在自己的手機／電腦裡。

## 直接改資料

所有內容都在 `trip.json`。在 GitHub 網頁上點檔案 → 鉛筆圖示就能改，存檔後約 1 分鐘網站更新。

- 每一天在 `days` 裡，行程項目在 `lanes[].items`，口袋名單在 `backups`。
- 每個項目：`time` 時間、`name` 名稱、`desc` 說明、`price` 費用、`map` 地圖搜尋字（韓文最準）、`gap: true` 代表待補。
- 新增項目時 `id` 隨便取一個不重複的字串就好。

## 「存到 GitHub」要的 token

到 GitHub → Settings → Developer settings → Fine-grained tokens → Generate new token：

1. Repository access 選 **Only select repositories**，只勾這個 repo。
2. Permissions → Repository permissions → **Contents: Read and write**。
3. 產生後貼到網頁的「存到 GitHub」視窗，可勾「記住在這台裝置」。

Token 只給管理的人用，不要貼到群組裡。其他家人用「分享給家人看」就好。

## 注意

GitHub Pages 是公開網頁，知道網址的人都看得到。不要把護照號碼、訂房代號、付款資料放進來。
