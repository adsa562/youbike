# 臺北市公共自行車「YouBike 微笑單車」租賃站資料轉換程式

這是一個用 Ruby 寫的小程式，可將 YouBike 微笑單車租賃站資料轉換為 [JOSM file format](http://wiki.openstreetmap.org/wiki/JOSM_file_format), CSV, JSON 三種檔案格式，以便後續再利用。

我寫這個程式的動機是想要最新、最正確的租賃站名稱、座標，以便不定時（譬如有新設的租賃點時）匯入 [OpenStreetMap](http://openstreetmap.org/)。如果您的用途是想要取得即時可借車輛數（耗費持續的資料傳輸流量）開發相關應用，請去[申請介接臺北市即時交通資訊](http://www.dot.taipei.gov.tw/ct.asp?xItem=3167481&CtNode=44829&mp=117001)。

## 使用方法

本程式遵循一般常見 Ruby 程式的部署方法，使用 Bundler 與 Gemfile 自動安裝必要元件。執行 <code>youbike.rb</code> 後，若過程無誤，則會在同樣位置產生 <code>youbike-export-$timestamp.osm</code>, <code>youbike-export-$timestamp.json</code>, <code>youbike-export-$timestamp.csv</code> 檔案。

## 參考資料

* [臺北市公共自行車租借站及價格資料](http://data.taipei.gov.tw/opendata/apply/NewDataContent?oid=7114B2ED-D8E5-49FD-81F9-F479806DB635#)
* [Tag:amenity=bicycle_rental - OpenStreetMap Wiki](http://wiki.openstreetmap.org/wiki/Tag:amenity%3Dbicycle_rental)
