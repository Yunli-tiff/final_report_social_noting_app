# 社群筆記牆 Community Note Wall

## 專案說明
此應用能自動將上傳的圖片（OCR）、音訊（Whisper 語音辨識）、純文字內容，透過 GPT 完成「摘要 + 主題分類」，並呈現在可搜尋、可匯出、可同步到 Notion / Dropbox 的互動式筆記牆中。

## 架構
- `app.py`：主程式 (Streamlit UI)
- `utils/ocr.py`：OCR 模組
- `utils/whisper_asr.py`：Whisper 語音辨識模組
- `utils/gpt.py`：GPT 摘要與主題分類模組
- `utils/search_filter.py`：搜尋 + 篩選功能
- `utils/markdown_export.py`：Markdown 匯出功能
- `utils/notion_api.py`：Notion 同步功能
- `utils/dropbox_export.py`：Dropbox 備份功能

## 安裝與執行

1. Clone 專案：
   ```
   git clone <your-repo-url>.git
   cd community_note_wall
   ```

2. 安裝相依套件：
   ```
   pip install -r requirements.txt
   ```

3. 設定環境變數：
   - `OPENAI_API_KEY`：你的 OpenAI API 金鑰
   - （選填）`NOTION_TOKEN`：Notion Integration Token
   - （選填）`DROPBOX_TOKEN`：Dropbox Access Token

4. 執行：
   ```
   streamlit run app.py
   ```

## 部署
可部署至 [Streamlit Cloud](https://streamlit.io/cloud)：
1. Push 至 GitHub。
2. 在 Streamlit Cloud 建立新應用並連結此 repo。
3. 設定 Secret 環境變數：`OPENAI_API_KEY`, `NOTION_TOKEN`, `DROPBOX
