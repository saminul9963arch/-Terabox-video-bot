# -Terabox-video-botma 
in.py
requirements.txt
Procfile
README.md (optional)
from pyrogram import Client, filters
import os

api_id = int(os.environ.get("API_ID"))
api_hash = os.environ.get("API_HASH"))
bot_token = os.environ.get("BOT_TOKEN")

app = Client("SamiteraBoxVdoBot", api_id=api_id, api_hash=api_hash, bot_token=bot_token)

@app.on_message(filters.command("start"))
async def start(client, message):
    await message.reply_text("✅ Wellcome and try terabox in bot version video")

@app.on_message(filters.text & filters.private)
async def link_handler(client, message):
    link = message.text
    if "terabox" in link:
        await message.reply_text(f"📥 Terabox Link Received:\n{link}\n\n✅ Video Downloading Feature Under Setup!")
    else:
        await message.reply_text("❌ Please send a valid Terabox link!")

app.run()
pyrogram
tgcrypto
worker: python main.py
# SamiteraBoxVdoBot
✅ Simple Terabox Telegram Bot
