ทีฆทัศน์ ทับเคลียว 6704800026

ประณาลี ทารัตน์ 6704800001

# โปรเจค Big Data - วิเคราะห์ข้อมูล Forex 📊

ระบบวิเคราะห์ข้อมูล Forex ด้วย Apache Airflow, Flask API และ React Dashboard

## 🔧 เทคโนโลยีที่ใช้
- Apache Airflow 3.x
- Flask + CORS
- React + TailwindCSS + Recharts
- Pandas + Parquet

## 📈 ฟีเจอร์
- ระบบ ETL อัตโนมัติ
- REST API สำหรับดึงข้อมูล
- Dashboard แบบ Real-time
- รองรับ 3 กรอบเวลา (D1, H1, H12)

## 📊 แหล่งข้อมูล
ข้อมูล Forex จาก Kaggle
- คู่เงิน 9 คู่ (AUDCAD, EURUSD, GBPUSD, ฯลฯ)
- 3 กรอบเวลา: รายวัน (D1), รายชั่วโมง (H1), 12 ชั่วโมง (H12)

## 🚀 วิธีติดตั้งและใช้งาน

### สิ่งที่ต้องติดตั้ง
- Python 3.13+
- Node.js 18+
- Docker (สำหรับ Airflow)

### ขั้นตอนการติดตั้ง

\`\`\`bash
# โคลนโปรเจค
git clone https://github.com/Theekhathan/Big_Data_Project.git
cd Big_Data_Project

# สร้าง virtual environment
python -m venv .venv
source .venv/bin/activate  # ถ้าใช้ Windows: .venv\Scripts\activate

# ติดตั้ง Python packages
pip install -r requirements.txt

# ติดตั้ง Node packages
cd forex-dashboard
npm install
cd ..
\`\`\`

### รันโปรแกรม

\`\`\`bash
# เทอร์มินอลที่ 1: เริ่ม Airflow
airflow standalone

# เทอร์มินอลที่ 2: เริ่ม Flask API
python api/app.py

# เทอร์มินอลที่ 3: เริ่ม React Dashboard
cd forex-dashboard && npm start
\`\`\`

### เข้าถึงโปรแกรม
- Airflow UI: http://localhost:8080
- Flask API: http://localhost:5000
- Dashboard: http://localhost:3000

## 📁 โครงสร้างโปรเจค

\`\`\`
Big_Data_Project/
├── api/              # Flask REST API
│   └── app.py
├── dags/             # Airflow DAGs
│   ├── forex_d1_etl_pipeline.py
│   ├── forex_h1_etl_pipeline.py
│  └── forex_h12_etl_pipeline.py
├── data/             # โฟลเดอร์ข้อมูล
│   ├── processed/    # ไฟล์ Parquet
│   └── raw/          # ไฟล์ CSV ดิบ
├── forex-dashboard/  # React frontend
│   ├── src/
│   │   └── App.js
│   └── package.json
├── scripts/          # สคริปต์ต่างๆ
├── .gitignore
├── README.md
└── requirements.txt
\`\`\`

## 📊 API Endpoints

- \`GET /api/pairs\` - รายชื่อคู่เงินทั้งหมด
- \`GET /api/data/{pair}?tf={D1|H1|H12}&limit=100\` - ดึงข้อมูล Forex
- \`GET /api/timeframes\` - รายชื่อกรอบเวลาที่มี
- \`GET /api/health\` - ตรวจสอบสถานะ

## 👨‍💻 ผู้พัฒนา
Theekhathan

## 📅 อัปเดตล่าสุด
พฤษภาคม 2026
