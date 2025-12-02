# 📊 Coders of Hyderabad — Instagram Data Analysis  
*A fun data-engineering challenge from Sam Altman*

## 📘 Story  
You ask Sam Altman for **$2.2 billion** in funding.  
He laughs, roasts you publicly, and gives you a 24-hour challenge:

> “Collect raw Instagram data of all OpenAI followers and answer:
> - Who has the **maximum posts**?
> - Who has the **maximum followers**?
> - Who follows the **maximum people**?
> - How many **categories** (Digital Creator, Non-Profit Organization, etc.) exist, and how many users belong to each?”

He refuses to give you the data —  
so you hire **Haris**  and **Sam**.  
You meet halfway at **Morninglab Café**, and begin the mission.

---

## 📂 Project Structure

├── finaldata.txt              # Raw final Instagram text data (scraped chunks) by Haris and Sam
├── coders_of_Hyderabad.ipynb  # Jupyter notebook with parsing + analysis
├── data.json                  # Final cleaned JSON output
├── intialdata.txt             # Raw Instagram text data (starting point)
└── README.md                  # This file


---

## 🛠️ What This Notebook Does

### ✔️ 1. Loads raw text data  
The file `finaldata.txt` contains Instagram data in messy text blocks.

### ✔️ 2. Splits data into chunks  
Each user entry is separated by blank lines.

### ✔️ 3. Parses each chunk  
From every profile, the script extracts:

- `username`
- `no_of_post`
- `no_of_followers` (K/M converted to numbers)
- `no_of_followings`
- `name`
- `type_of_page`
- `bio`

### ✔️ 4. Cleans numeric fields  
Example:
- `"2.5K followers"` → `2500`
- `"1.2M followers"` → `1200000`


---

## 📈 Analysis Performed

### 🥇 **1. Who has the maximum posts?**
The notebook loops through `all_chunks` and finds the user with the highest `no_of_post`.

### 🥇 **2. Who has the maximum followers?**
Same logic but based on `no_of_followers`.

### 🥇 **3. Who follows the most people?**
Checks `no_of_followings`.

### 🏷️ **4. How many categories exist?**
Counts unique `type_of_page` values (Digital Creator, Public Figure, etc.)

---

## 🚀 How to Run (Script Style)

```bash
# Clone the Repository

git clone https://github.com/Waqas721/Coders_Of_Hyderabad
cd Coders_Of_Hyderabad
```

## 📦 Output Files
-  Categories summary
-  Maximum posts
-  Maximum followers
-  Maximum followings

## 🤝 Contributing!

### Ideas for improvement:
- ✔ Add more advanced analytics
- ✔ Add charts & visualizations
- ✔ Support CSV / Excel export
- ✔ Catch additional edge cases
- ✔ Automatic data scraping module

### Steps to contribute:
fork → branch → commit → push → pull request

## ⭐ Support
If this project helps you, star ⭐ the repo to support it!








