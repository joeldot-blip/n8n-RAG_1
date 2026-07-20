# n8n-RAG_1
This RAG project was inspired by my interests in the finance world and my problem with reading 100 pages of Due Diligence reports and then taking a few more hours to fully understand the thesis.
Using a RAG workflow ensures that there is a lot less guessing on the AI's side and increased responsibility on the data source in the event of a wrong/incorrect output as opposed to trying to guess where the problem stems from

Heres how the workflow sequence looks like:
~The workflow uses the Google Drive API to download my uploaded finance reports (in .pdf format, but can realistically be run with really any text based format) into the workflow
~The downloaded file is then broken down into chunks and is stored in a vector Database (I use Supabase as my database)
~I have my Google Gemini API connected and my Telegram Bot connected 
~Now, whenever I send a prompt through my Telegram Bot, it sends my prompt to Google Gemini and the AI uses ONLY the data stored in the vector Database to respond to my request

Tools used:
~n8n
~Supabase
~Google Drive
~Google Gemini
~Telegram
~Original Finance report from Micheal Burry's substack
