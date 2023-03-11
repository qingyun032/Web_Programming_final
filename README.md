# [111-1] Web Programming Final

## (Group 70) 超級行事曆

**Demo 影片連結:**

- https://youtu.be/WtA7uUGoXvw
- https://drive.google.com/file/d/1KTXN7gP_SFMYQnwzEqC4-Iq5DOMPBfZH/view?usp=sharing
- 建議使用 youtube 畫質較高

**Deploy 連結:**

- wpfinal-production.up.railway.app
- https://wp-final.onrender.com
- 用 railway 比較快，但他可能撐不到評分的時候（？

## 描述這個服務在做什麼

整合行事曆與 To Do List ，方便規畫個人生活。在行事曆中可依個人喜好，用顏色區分不同類型的事件。在 TO Do List 可直觀的看到最快要截止的事件，也可用 filter 篩選事件類別。完成的事件在 Calendar 中會有刪除線，方便區分是否完成，讓使用者能更專注在未完成的事件上。

## 操作方法

#### 登入畫面

- 可點選下方 **not a member? click here!** 註冊會員
- 輸入 username 和 password 登入
- 可直接用 tab 切換輸入格，若完成填寫後按 enter 則可直接送出，使操作更加便捷直觀

#### 主畫面

- **Calendar**
  - 可切換 month 、 week 、 day 模式
  - 點擊日期可以新增事件
    - 可選擇是否為整天事件，若不是整天事件則可以選擇時間
    - 可選擇是否要加入事件到 To Do List
    - 可選擇顏色分類事件
  - 點擊事件會顯示該事件的內容
    - 可選擇要刪除或更新事件
- **To Do List**
  - 上方有 filter 可以用顏色篩選事件
  - 事件根據結束時間排序，越早結束的事件越上面
  - 勾選 check box 後 To Do List 和 Calendar 的事件會有刪除線，讓使用者能在 Calendar 介面清楚得知還有哪些事件未完成
  - 點擊事件會顯示該事件的內容
    - 可選擇要刪除或更新事件
  - 點擊刪除按鈕可刪除事件
- **Setting**
  - 可更新 display name 及 password
  - display name 為顯示在導覽列上方的文字，非登入時的 username
- **Log out**
  - 點擊後會再次詢問是否要登出，若確認登出會返回登入畫面

## 未來更新

- **自訂分類名稱**
  - 現行功能為自己選擇顏色分類，未來可為不同顏色命名，更為直觀
- **群組功能（整合 Calendar)**
  - 群組功能整合成員行事曆，可看到其他使用者的時間規劃，有助於安排團體活動
- **提醒功能**
  - 可設定於活動前多少時間提醒，時間一到會跳出視窗警示

## 使用與參考之框架/模組/原始碼

#### frontend

- react
- react-router-dom
- antd
- axios
- uuid
- react-fullcalendar
- dayjs

#### backend

- express
- cors
- bcrypt
- dotenv-defaults
- mongoose

#### database

- MongoDB

## 安裝與測試步驟

#### frontend (在 `localhost:3000`)

- 在 `final/frontend`
  ```
  yarn
  yarn start
  ```

#### backend (在 `localhost:4000`)

- 在 `final/backend/` 新增 `.env`
  ```
  MONGO_URL= //your database url
  ```
- 在 `final/backend/`
  ```
  yarn
  yarn server
  ```

## 工作分配

#### 廖奕鈞：

- 前端架構
- 前端設計(css)
- deploy 與報告撰寫
- 作品測試

#### 張晴昀：

- 後端架構
- 前後端連接
- 前端架構
- 報告撰寫
- 作品測試

#### 吳岱凌：

- 影片錄製
- 作品測試
- 前端微調

## 專題製作心得

#### 廖奕鈞：

這次是我第一次接觸到全端 project，深刻感受到合作與團隊分工的重要性。起初因其他課程而較晚起步，開始時與張晴昀合作時效率極差，常常發生雖然我們有兩台電腦，兩個人也坐在一起，但只有一個人可以做事，另外一個人只能看著的狀況。而經過磨合後效率大幅提升，中期開始就可以邊做自己的部分邊跟對方討論哪些需要修正。此次選擇做超級行事曆是看到現有的行事曆程式中的缺陷，希望能用課程所學優化現有問題，因此期許這個作品不只是一份作業，而是未來能夠繼續使用、為生活帶來便利的成品，這也是為什麼會規劃未來更新的部分。從無到有的生出一個網站讓我對前後端有更深的理解，也讓我擁有寶貴的合作經驗，學會如何與他人溝通、交流與激盪想法、共同撰寫專案。

#### 張晴昀：

這次 project 要從頭開始設計一個網頁，和學期中的作業有 sample code 可以參考不同，我們需要設計前端畫面、每個功能該如何實作及前後端連結的方式等等，許多事情都需要好好考慮。一開始，我先將前端架構架好後再著手完成後端的 api ，最後大家一起完善各項功能並修改 css ，其中我遇到最大的困難是不熟悉 fullcalendar 的使用方法，且他和 antd 的日期格式不同，需要再進行轉換。這次製作網站讓我更了解這學期所學，之前囫圇吞棗的地方也慢慢有了新的認識，希望之後能繼續學習前後端的應用。

#### 吳岱凌

這次的 final project 我是負責後面的 demo 影片以及測錯的工作，在程式碼部分沒有貢獻那麼多，但在最後的統整以及試圖呈現整個作品的過程中，我深刻的了解要完成一項全端作品的難度所在：從前端的 html 和 css 的架構到後端連接，再到最後的美化和側錯的環節，每一項都相當的耗時且花費耐心，這次的作業統整了我整個學期以來許多茫然的知識，因為之前的作業都是要求我們完成部分的內容，而藉由完成整份全端 project，我的理解也更加通徹。很慶幸有兩位厲害的組員帶領完成整份 project，也很期待我們的這個作品可以在未來可以更加完善並且真正解決現有行事曆和代辦事項所遇到的障礙。
