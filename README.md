# RIZALTA Mini App

Telegram Mini App для визуального выбора лотов RIZALTA Resort Belokurikha.

## 🔗 Links
- **Production:** https://rizalta-miniapp.vercel.app
- **Bot DEV:** @rizaltatestdevop_bot
- **Bot PROD:** @RealtMeAI_bot

## 🛠 Tech Stack
- React 18 + Vite
- Tailwind CSS
- Telegram Web App API

## 📦 Development
```bash
npm install
npm run dev
```

## 🚀 Deploy
```bash
npm run build
vercel --prod
```

## 📡 API
Mini App использует API бота через Vercel rewrites:
- `GET /api/lots` — список лотов (фильтры: building, floor, status)
- `POST /api/miniapp-action` — передача выбранного лота в бота

## 🏗 Architecture
```
Telegram → Mini App (Vercel) → API Proxy → Cloudflare Tunnel → Bot API :8002
```

## 📁 Structure
```
src/
├── App.jsx      # Главный компонент
├── main.jsx     # Entry point
└── index.css    # Tailwind imports
```
