你是一位前端工程師。請幫我製作一個單一檔案的前端小系統，輸出完整 index.html。

系統名稱：XXX_SYSTEM_NAME
資料主體：XXX_RECORD_NAME

使用者輸入欄位：
1. XXX_FIELD_1：XXX_FIELD_1_LABEL，必填
2. XXX_FIELD_2：XXX_FIELD_2_LABEL，必填
3. XXX_FIELD_3：XXX_FIELD_3_LABEL，可選

每筆 record 必須包含：
1. id：唯一識別
2. createdAt：建立時間，用 new Date().toISOString()
3. status：預設 active，可以切換成 done
4. XXX_FIELD_1
5. XXX_FIELD_2
6. XXX_FIELD_3

功能要求：
1. 使用者可以透過表單新增一筆 XXX_RECORD_NAME。
2. 新增後，資料會即時顯示在頁面上。
3. 頁面要用 XXX_DISPLAY_STYLE 顯示所有資料。
4. 每筆資料要有 status，預設 active。
5. 每筆資料要有一個按鈕，可以在 active 和 done 之間切換。
6. done 的資料在畫面上要顯示成「XXX_STATUS_DONE_TEXT」狀態，並且視覺上和 active 有分別。
7. 頁面要有 filter：全部 / active / done。
8. 資料要用 localStorage 儲存，刷新頁面後仍然存在。

技術要求：
1. 只可以輸出一個 index.html。
2. 不要使用 React、Vue、Vite、Firebase 或任何 backend。
3. HTML、CSS、JavaScript 全部寫在同一個檔案。
4. localStorage key 固定叫 records。
5. 每筆 record 必須包含：
   - id
   - createdAt
   - status
   - 以及我這個主題需要的 2-4 個欄位
6. JavaScript 必須清楚分開以下 function：
   - createRecord()
   - saveData(record)
   - loadData()
   - renderList()
7. function 職責要固定：
   - createRecord(formData)：根據表單內容建立一筆新 record object。
   - saveData(record)：只負責新增一筆 record 到 records array，然後寫入 localStorage。
   - loadData()：從 localStorage 讀取 records array；沒有資料就回傳 []。
   - renderList(recordsToShow)：把 records 顯示到頁面。
   - updateRecord(id, changes)：只負責更新一筆 record，然後寫入 localStorage。
8. 不要把示範資料寫死在 HTML 裏面。
9. 不要只做靜態展示頁，必須真的可以新增、保存、讀取、filter。

輸出格式：
1. 先列出 Data Contract，說明每個欄位用途。
2. 再輸出完整 index.html。
3. 除了 index.html，不要輸出其他檔案。