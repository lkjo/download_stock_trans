# 每日成交統計表程式

此程式用於擷取特定日期範圍內的股票每日成交統計資料，並將其存儲為 Excel 文件。

## 使用的模組及其描述：

- `xml.etree.ElementTree`: 負責解析 XML 檔案。
- `requests`: 基本的網頁爬蟲指令，用於向網站發送請求並獲取回應。
- `time`: 用於時間間隔，確保不會過於頻繁地發送請求。
- `openpyxl`: 負責創建和編輯 Excel 文件。

## 主要功能：

1. 從 `setting.xml` 讀取設定。
2. 根據日期範圍，生成需要請求的日期列表。
3. 透過爬蟲，抓取每日的成交統計資料。
4. 將擷取到的資料保存為 Excel 文件。

## 使用方式：

由於此程式碼已轉換為 `.exe` 執行檔，所以只需雙擊執行即可。

但需確保 `setting.xml` 設定檔與 `.exe` 執行檔在同一目錄下。

## `setting.xml` 設定檔說明：

- `<url>`: 資料來源網址。
- `<excelName>`: 輸出的 Excel 文件名稱。
- `<startYear>` & `<startMonth>`: 起始年份與月份。
- `<endYear>` & `<endMonth>`: 結束年份與月份。
- `<stockNo>`: 股票代號。

範例：

```xml
<params>
  <url>https://www.twse.com.tw/rwd/zh/afterTrading/STOCK_DAY</url>
  <excelName>宏達電202101_202306</excelName>
  <startYear>2021</startYear>
  <startMonth>01</startMonth>
  <endYear>2023</endYear>
  <endMonth>06</endMonth>
  <stockNo>2498</stockNo>
</params>

---

您現在可以直接複製上述內容並粘貼到您的 `readme.md` 檔案中。
