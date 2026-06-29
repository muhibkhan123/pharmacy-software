🏥 Pharmacy Management System (PMS)

A comprehensive, offline-first, single-page Web Application designed to manage pharmacy operations efficiently. It features a complete Point of Sale (POS) system, inventory management, Khata (Ledger) tracking for both customers and suppliers, detailed P&L accounting, and barcode scanning/printing capabilities.

✨ Key Highlights

⚡ Offline-First Architecture: Runs entirely in the browser utilizing LocalStorage (No backend database required).

🌍 Bilingual Support: Seamlessly switch between English (LTR) and Urdu (RTL) interfaces.

🔐 Role-Based Access Control (RBAC): Restrict system access based on user roles (Super Admin, Admin, Cashier) with granular module-level permissions.

🖨️ Thermal Printer Ready: Dedicated print stylesheets optimized for 80mm thermal receipt printers.

📷 Integrated Barcode System: Generate (Code128) and scan barcodes using a device camera or external barcode scanner.

📊 Advanced Analytics: Built-in dashboard with Chart.js visualizations for sales trends and inventory distribution.

📂 Modules & Features (Tab by Tab)

1. 🏠 Dashboard

Quick Actions: New Sale, Add Medicine, Scan Barcode, New Purchase, Print Barcodes (Single/Bulk).

KPI Cards: Total Sales, Available Meds, Net Profit, Total Udhaar, Total Expenses, Current Stock Value, Expected Profit.

Visual Charts: 7-Day Sales Trend (Line Chart) & Inventory Distribution (Doughnut Chart).

Live Widgets: Recent Sales feed and Low Stock/Expiry Alerts table.

2. 🛒 POS & Inventory

Sales (POS Terminal): - Scan barcode or search by name/formula.

Cart management with Hold Cart / Restore Cart functionality.

Payment routing (Cash or Credit/Udhaar).

Apply discounts (Rs or %) and Tax/GST (%).

Quick-tap items grid for fast selling.

🧾 Cash Register (Shift Management):

Open/Close drawer shifts with an opening balance.

Auto-calculation of expected drawer cash based on daily cash sales.

📦 Purchases (GRN):

Record incoming stock from suppliers (Cash or Credit).

Auto-updates inventory stock levels and purchase prices.

💊 Medicines:

Add/Edit items with Name, Category, Formula, Batch, Purchase/Sale Price, Min Stock, and Expiry.

Single & Bulk Barcode generation & PDF export.

Dynamic Sub-Views: Total Medicines Sold, Every Single Medicine, Low Stock Medicines.

🏢 Inventory:

High-level overview of total catalog items and low-stock count.

3. 👥 People & Khata

👥 Customers (Khata/Ledger):

Manage walk-in or regular customers.

Ledger System: Track Udhaar (Debit) and Jama (Credit).

Add manual adjustments, edit ledger entries, and print customer ledgers.

🚚 Suppliers:

Track payable balances (Maal Aya vs Paid).

Complete supplier ledger and thermal printouts.

👷 Employees & 🛵 Delivery:

Track staff roles and monitor pending/delivered orders.

4. 💸 Finance & Reports

💸 Expenses (Kharchay):

Track shop expenses by category (Rent, Salary, Bills, etc.).

📊 P&L Accounting:

Real-time calculation of Total Sales Revenue, COGS, Total Expenses, and Khaalis Munafa (Net Profit).

📈 Sales Reports:

Date-filtered sales history.

Return Mechanism: Handle returns via Cash Refund or Khata Reversal.

Edit past sales, reprint receipts, or export the entire report to Excel (.xlsx).

⚠️ Alerts:

Auto-generated warnings for Low Stock, Expiring Soon (90 days), and Expired medicines.

5. ⚙️ System

🛡️ Users & Roles (Super Admin):

Create and manage user credentials.

Create custom roles with specific module access checkboxes.

⚙️ Settings:

Customize Pharmacy Name, Address, Contact, and Upload Shop Logo (reflects on UI and printed receipts).

💾 Backup & Restore:

Download entire database as a .json file for safe-keeping.

Restore database from backup file.

💀 Danger Zone (Factory Reset):

Hard reset the entire system (Requires secure superadmin key).

🛠️ Technology Stack

Technology

Usage

HTML5 / CSS3

Core structure and styling (Custom Variables + Print Media Queries)

Vanilla JS (ES6)

Core logic, state management, DOM manipulation

Bootstrap 5.3

Responsive Grid, Modals, Toasts, Badges

FontAwesome 6.4

System Icons

Chart.js

Dashboard analytics and visualizations

JsBarcode

Generating CODE128 barcodes for medicines

Html5-Qrcode

Browser-based barcode/QR scanning via device camera

jsPDF / AutoTable

Generating and downloading PDF reports

SheetJS (xlsx)

Exporting sales data to Excel

🚀 Installation & Usage

Because this application is built with an offline-first, client-side architecture, installation is practically instantaneous.

Clone the repository or download the .zip.

Extract the files.

Simply double-click the index.html file to open it in any modern web browser (Chrome, Edge, Firefox, Safari).

No local server (XAMPP/Node) is required!

🔑 Default Login Credentials

(Assuming initial system setup)

Super Admin: superadmin / superadminmuhib

Admin: admin / admin123

Cashier: cashier / pos123

🖨️ Printing Configuration

For the best thermal printing experience (80mm):

Complete a sale in the POS to trigger the print dialog.

Under printer settings, set Paper Size to 80mm Roll (or equivalent).

Set Margins to None.

Uncheck Headers and Footers.

Ensure "Background Graphics" is enabled if you want the logo to print properly.

🔒 Security & Data Privacy

Local Storage: All data (pharmacySysDB) is saved directly in the user's browser localStorage. No data is sent to external servers.

Backups: It is highly recommended to use the Settings > Database Backup feature weekly to prevent data loss in case browser cache is cleared.

Factory Reset Keys: The system contains hardcoded reset keys (muhib-1234, Latif-1, mohammad-1) to prevent accidental data erasure by standard admins.

Built with ❤️ for Pharmacies requiring fast, local, and reliable management software.