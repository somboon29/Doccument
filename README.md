forex-app/
├── backend/
│   ├── app/
│   │   ├── main.py              # FastAPI entrypoint
│   │   ├── db.py                # Database connection (SQLAlchemy 2.0)
│   │   ├── models.py            # ORM models: MarketTick, NewsItem, CalendarEvent
│   │   ├── schemas.py           # Pydantic schemas
│   │   ├── services/
│   │   │   └── market_provider.py   # ดึงข้อมูลราคาจาก API ภายนอก
│   │   ├── utils/
│   │   │   └── indicators.py        # ฟังก์ชันคำนวณ SMA, EMA, RSI ฯลฯ
│   │   ├── tasks.py             # Scheduler jobs (poll market, fetch news)
│   │   └── __init__.py
│   ├── requirements.txt
│   └── Dockerfile
│
├── frontend/
│   ├── src/
│   │   ├── main.js              # Vue 3 entrypoint
│   │   ├── App.vue
│   │   ├── components/
│   │   │   ├── MarketChart.vue  # กราฟแสดงราคา
│   │   │   ├── NewsList.vue     # ข่าว Forex
│   │   │   └── CalendarView.vue # ปฏิทินเศรษฐกิจ
│   │   ├── stores/
│   │   │   └── market.js        # Pinia store (market data)
│   │   └── api/
│   │       └── client.js        # axios client
│   ├── package.json
│   └── vite.config.js
│
├── docker-compose.yml           # รวม backend + frontend + db
└── README.md