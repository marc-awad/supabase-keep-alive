# 📦 supabase-keep-alive

This repository contains a **GitHub Action workflow** that keeps a Supabase project active by automatically sending a weekly HTTP request to the project's URL.

---

## ⚙️ Purpose

Supabase automatically pauses inactive projects after 7 days of inactivity on free plans.  
This script helps you avoid that limitation **at no cost** and with **zero manual effort**.

---

## 🚀 How It Works

- **Frequency:** Once per week (every Monday at 8 AM UTC)
- **Action:** Sends a `GET` request to the public Supabase project URL (API or frontend)
- **Result:** Activity is detected, preventing automatic pausing

---

## 🛠 Requirements

- An active Supabase project
- Your project’s public URL  
  _(found in Supabase → Project settings → API → Project URL)_

---

## 🧪 Manual Execution 

You can manually trigger the workflow from the **Actions** tab in GitHub if needed.

---

## 📝 Notes

- The script uses `curl -I` to send a lightweight `HEAD` request.
- You can customize the frequency or the target URL in the `keepalive.yml` file to suit your needs.
