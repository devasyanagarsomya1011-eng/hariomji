# Shree Ram Medical — Billing & Reports

Persistent, server-side pharmacy billing application. It uses a SQLite relational database stored beside the server (`data/shreeram.db`), never browser storage.

## Run

```bash
cd /Users/devasyanagar/Documents/Codex/2026-08-10/build/outputs/shreeram-medical-billing
npm start
```

Open http://localhost:3000. The first run creates the database, tables, and a small starter medicine catalog.

## Included

- Relational tables for users, customers, doctors, medicines, batches, suppliers, purchases, purchase items, sales, sale items, payments, expenses, settings, and audit logs.
- Transactional sale save/cancel flows that update stock and preserve cancelled bills.
- Searchable bill history and bill actions: view, edit (re-open draft), reprint, PDF, Word, and Excel.
- Real `.xlsx`, `.docx`, and `.pdf` generation from database records—no placeholder export buttons.
- Filterable reports and database backup / restore endpoints for an administrator.

The server is deliberately dependency-free: Node's built-in `node:sqlite` supplies the persistent database and the exports are generated as standards-compliant files.
