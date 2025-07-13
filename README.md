# Kala Vastralya – Retail Management System

A full‑stack, offline‑first web app designed for local clothing stores to manage inventory, record sales & estimates, print bills, and generate detailed reports. Built with React, Node.js, Express, and SQLite—optimized for Indian Standard Time (IST, GMT+5:30).

---

## 🔍 Project Description

Kala Vastralya helps shop owners:

- **Manage Inventory**  
  Add/update products by barcode, category & manufacturer. Track stock levels in real time.

- **Record Sales & Estimates**  
  Create bills (`BILL-XXXX`) or estimates (`EST-XXXX`) with optional customer info, dynamic discount/“To Pay” controls, and optional payment mode.

- **Print & Export**  
  Generate printable receipts. Import/export products via Excel. Export filtered sales/estimates to Excel.

- **Sales Reporting**  
  View/filter/search all transactions (by date, type, customer name/mobile). Edit or return items, auto‑adjust inventory & totals.

- **Offline‑First**  
  Entirely local—no internet required. All data lives in a SQLite file.

---

## 🚀 Key Functionalities

| Feature                   | Details                                                                 |
|---------------------------|-------------------------------------------------------------------------|
| Inventory Management      | Barcode scan/input, add categories & manufacturers on the fly, stock updates |
| Billing & Estimates       | Auto bill/estimate numbering, “Walk In Customer” default, dynamic discount & final amounts |
| Optional Payment Mode     | Cash/UPI selection (not required)                                        |
| Excel Integration         | Import products, export inventory or filtered sales/estimates            |
| Sales Report              | Date & range filters, type filter, global search, edit/return items      |
| IST Date & Time           | All timestamps stored & displayed in Asia/Kolkata timezone               |
| One‑Click Launch          | `start-app.bat` to install & run both frontend/backend and open browser  |

---

## 🗂️ File Structure

```

kala-vastralya-ledger-book/
├── .gitignore
├── package.json
├── prd.txt
├── README.md
├── start-app.bat             ← one‑click launcher
├── data/
│   └── kalan_vastralya.db     ← SQLite database file
├── public/
│   ├── favicon.ico
│   └── robots.txt
├── src/
│   ├── App.tsx
│   ├── main.tsx
│   ├── server/
│   │   └── index.cjs         ← Express + SQLite backend
│   ├── components/           ← UI components
│   ├── contexts/             ← React Context API
│   ├── lib/                  ← API helpers
│   └── pages/                ← Route pages (Inventory, NewSale, SalesReport, etc.)
├── tailwind.config.ts
└── vite.config.ts
```

## 📥 Download & Setup

1. **Clone the repo**  
```bash
   git clone https://github.com/<your‑username>/kala-vastralya-leger-book.git
   cd kala-vastralya-ledger-book
````

2. **Install Node.js**
   Download & install the LTS version from [nodejs.org](https://nodejs.org).

3. **Install dependencies**

   ```bash
   npm install
   npm install concurrently --save-dev
   ```

---

## ⚙️ Running the App

### ▶️ One‑Click (Windows)

Double‑click **`start-app.bat`** in the project root.
This will:

1. Launch backend & frontend via `npm run dev-all`
2. Wait a few seconds
3. Open your default browser at `http://localhost:8080/`

### ▶️ Manual

**Backend**

```bash
node src/server/index.cjs
```

**Frontend**

```bash
npm run dev
```

Then open:

```
http://localhost:8080/
```

---

## 🔧 Configuration

* **Ports**

  * Frontend: 8080 (configured in `vite.config.ts`)
  * Backend: 3001 (default, override via `PORT` env var)

* **Database**

  * Located at `data/kala-vastralya.db`
  * Automatically initialized on first run

* **Environment Variables**
  You can set `PORT` to change the backend port. Otherwise it defaults to 3001.

---
