# Receipt Product Tool

A Windows desktop application for OCR-based Japanese receipt recognition and Rakuten product matching.

## Project purpose

This application helps users identify products listed on Japanese retail receipts. It reads receipt images with OCR, extracts product names, quantities and prices, then searches Rakuten Ichiba for possible matching products.

The Rakuten API data is used only to help the user verify OCR results. The application may retrieve:

- Product name
- Product price
- Product image
- Shop name
- Product URL

The application does not automatically purchase products and does not collect Rakuten account credentials.

## Main workflow

1. Import one or more receipt images.
2. Detect and enhance the receipt area.
3. Run Japanese OCR.
4. Parse product name, quantity, unit price and subtotal.
5. Search Rakuten Ichiba for candidate products.
6. Display the results in an editable table.
7. Export verified results to Excel or CSV.

## Planned technology

- Python 3.12
- PySide6
- PaddleOCR / PaddlePaddle
- pandas
- OpenCV
- Rakuten Ichiba Item Search API

## Rakuten API usage

- Expected request rate: approximately 1 request per second or less
- API calls are initiated by the user
- Search results are shown only for product verification
- API credentials are stored locally and are not committed to this repository
- Affiliate functionality is not required

The finished application will display the required Rakuten attribution, including **Supported by Rakuten Developers**, according to Rakuten Web Service requirements.

## Privacy

Receipt images and OCR results are processed locally on the user's Windows computer. API requests contain only product-search keywords required to find candidate products.

## Security

Do not commit any of the following:

- Rakuten Application ID
- Rakuten Access Key
- Brave, Tavily or other search API keys
- Receipt images containing personal information
- Local configuration files

## Status

The desktop application is currently under development.

---

## 中文說明

本專案是 Windows 桌面版日本發票辨識工具，主要用途如下：

1. 匯入日本發票照片。
2. 使用 OCR 辨識日文商品名稱、數量及價格。
3. 呼叫 Rakuten Ichiba 商品搜尋 API 尋找可能對應的商品。
4. 將候選商品名稱、價格、圖片、店家與網址顯示在可編輯表格中。
5. 由使用者確認後匯出 Excel 或 CSV。

Rakuten API 僅用於協助確認 OCR 辨識結果，不會執行自動購買，也不會收集 Rakuten 帳號密碼。
