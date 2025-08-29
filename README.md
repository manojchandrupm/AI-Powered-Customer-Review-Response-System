# AI-Powered Customer Review Response System

This project helps businesses automatically generate warm and genuine replies to customer reviews.  
Instead of manually writing responses to every single review, this system uses **AI (LLaMA 3 via Ollama)** to create short, friendly, and personalized replies that sound natural.

---

## ✨ Features
- Reads customer reviews (and reviewer names) from an Excel sheet.  
- Generates short 2–3 sentence replies that sound like a real business owner.  
- Ensures replies are **warm, polite, and context-aware**.  
- Processes reviews in **batches** to keep things efficient and stable.  
- Saves all the replies back into a new Excel file.

---

## 🛠️ Tech Stack
- **Python** (pandas, time)  
- **Ollama** (for running LLaMA 3 locally)  
- **Excel (pandas + openpyxl)**  

Hardware:  
- GPU: NVIDIA GeForce RTX 3050 (CUDA enabled)  
- Runs locally without needing cloud APIs.  

---

## 🚀 How It Works
1. Load reviews from `Reviews sample set.xlsx`.  
2. For each review:
   - Extract `review_text` and `reviewer_name`.  
   - Pass them into the AI model via **Ollama**.  
   - Generate a short, genuine reply.  
3. Collect all replies in batches.  
4. Save results into `reviews_with_replies.xlsx`.

---

## 📂 Example Output
| reviewer_name | review_text                            | reply                                                                 |
|---------------|----------------------------------------|----------------------------------------------------------------------|
| John          | "Great service and friendly staff!"     | "Thanks so much, John! We're glad you enjoyed the service and look forward to seeing you again." |
| Priya         | *5-star rating, no text*               | "Thank you, Priya, for your 5-star rating! Your support means a lot to us." |

---

## ⚡ Getting Started

### 1. Clone this repo
```bash
git clone https://github.com/yourusername/Reply_To_User_Reviews.git
cd Reply_To_User_Reviews
```
### 2. Install dependencies
```bash
pip install pandas openpyxl ollama
```
### 3. Run Ollama (make sure you have it installed)
```bash
ollama run llama3
```
### 4. Run the script
```bash
python main.py
```
