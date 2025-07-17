فایل main.py

import telebot import os

✅ توکن ربات را از متغیر محیطی دریافت می‌کنیم (امن‌تر)

TOKEN = os.getenv("7227213916:AAEqslEJI7dhdWyLrMTVeUrnK9Sa60WjYnY") bot = telebot.TeleBot(TOKEN)

@bot.message_handler(commands=['start']) def send_welcome(message): bot.send_message( message.chat.id, "🌟 به ربات VIPZEXNET خوش آمدید!\nبرای اجرای برنامه روی لینک زیر کلیک کنید:\n\n" "📲 https://mahdishamiahar.github.io/VIPZEXNETBOT/" )

@bot.message_handler(func=lambda m: True) def reply_menu(message): if message.text == "📩 دریافت نرم‌افزار": bot.send_message(message.chat.id, "📥 لینک نرم‌افزار: https://mahdishamiahar.github.io/apVIPZEXNET/") elif message.text == "🌐 سایت رسمی ربات": bot.send_message(message.chat.id, "🌍 وب‌سایت: https://mahdishamiahar.github.io/Web.VIPZEXNET/") elif message.text == "💬 پشتیبانی": bot.send_message(message.chat.id, "🧑‍💻 پشتیبانی: @Supp_ort_VIPZEXNET") elif message.text == "💳 خرید سرویس": bot.send_message(message.chat.id, "💸 برای خرید به پشتیبانی پیام بده: @Supp_ort_VIPZEXNET") elif message.text == "📱 باز کردن برنامه": bot.send_message(message.chat.id, "📲 اجرای مستقیم برنامه: https://mahdishamiahar.github.io/VIPZEXNETBOT/") else: bot.send_message(message.chat.id, "❗ لطفاً یکی از گزینه‌های منو را انتخاب کنید.")

bot.infinity_polling()
