# 📱 Power BI Project – UPI Transactions Analysis

## 🔗 Dashboard Link : 
https://app.powerbi.com/groups/7bd2401d-7ffd-4f3c-8a5c-7a2c5d060ef5/reports/26b87818-3227-4cec-9cad-68bd7a4eeff0/826aa75001275013d5b5?experience=power-bi&bookmarkGuid=11d1cd69d7ca0b19e991

## 🧩 Problem Statement

This dashboard analyzes UPI transaction data to understand transaction trends, balances, customer behavior, and usage patterns using interactive visuals and filters.


## ⚙️ Steps Followed

### 📥 Data Loading & Validation
- Loaded UPI Transactions dataset into Power BI Desktop  
- Verified data types for all columns  
- Converted **CustomerAccountNumber** and **MerchantAccountNumber** to **Text**

---

### 🕒 Transaction Time Transformation
- `TransactionTime` column contained **Date + Time**
- Requirement was **Time only**
- Used **Split Column → By Delimiter (Space) → Right-most**
- Removed date column and retained time component

---

### 🧪 Power Query – Data Profiling
Enabled from **View tab**:
- Column distribution  
- Column quality  
- Column profile  
- Profiling based on **entire dataset**



### 👥 Age Group Column (DAX)
     IF(
    'UPI Transactions'[CustomerAge] <= 25, "A1",
    IF('UPI Transactions'[CustomerAge] <= 35, "A2", "A3"))
---

## 📊 Page 1 – Overview

### 🎛 Slicers Used
- BankNameSent  
- BankNameReceived  
- City  
- DeviceType  
- Gender  
- Age Group  
- MerchantName  
- PaymentMethod  
- Purpose  
- TransactionType  

### 📈 Visuals
- Line Chart: **Transactions by Month**  
- Proper visual alignment and formatting applied  

### 📊 Dashboard Visual
**Power BI Service Dashboard**
![Image](https://github.com/user-attachments/assets/26391438-db12-4098-888a-7bdd7b82c571)

![Image](https://github.com/user-attachments/assets/15dfe39f-d577-419f-bc68-1fb758ce6d79)

---

## 📊 Page 2 – Detailed Analysis
- Same **10 slicers** used as Page 1  
- Matrix table for detailed transaction insights  
![Image](https://github.com/user-attachments/assets/d4eed28c-cbcc-47da-9d20-b6faa09d8d31)

---

### 🔄 Sync Slicers
- Used **View → Sync Slicers**  
- Enabled slicers across **Page 1 & Page 2**  
- Filters applied on one page reflect on the other  

![Image](https://github.com/user-attachments/assets/180e2b33-9bb7-413d-9456-b4e1252b0177)

---

## 🎨 Conditional Formatting
- Applied to **Amount** and **Remaining Balance**  
- Color scale:
  - Minimum → White  
  - Maximum → Purple  


---

## 🔖 Bookmarks & Navigation

### Dynamic Chart Switching
- **Amount**
  - Line Chart  
  - Column Chart  
- **Balance**
  - Line Chart  
  - Column Chart  

### Steps Followed
- Used **Selection Pane** to show/hide visuals  
- Created and **updated bookmarks after each change**  
- Added **Bookmark Navigator** for user interaction  

![Image](https://github.com/user-attachments/assets/f1bd7f80-c52f-44f0-bf3c-faf3f1ce1d07)
---

## 🛠 Tools & Technologies
- Power BI Desktop  
- Power Query  
- DAX  
- Data Modeling  
- Sync Slicers  
- Bookmarks  

---

## ✅ Conclusion
This UPI Transactions dashboard delivers an interactive and flexible analysis using slicers, synced pages, conditional formatting, and bookmarks. It helps stakeholders explore transaction trends, balances, and customer behavior efficiently, enabling data-driven decision-making.

