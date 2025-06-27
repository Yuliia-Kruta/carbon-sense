# 🌱 CarbonSense – Soil Carbon Analysis Made Simple

<img src="./carbon-sense.gif"/>

**CarbonSense** is a cloud-based web application developed as part of the **ICT Industry Project** at the University of the Sunshine Coast. Over the course of three months, our team worked in collaboration with industry partners to build a proof-of-concept system that enables rapid, low-cost prediction of soil carbon levels from coastal wetlands using data from portable NIR spectrometers.

🔗 **Live demo:** [https://unisc-carbon-sense.vercel.app](https://unisc-carbon-sense.vercel.app)

> ⚠️ **Note:** The source code for this project is not publicly available due to academic and client confidentiality agreements. This repository exists for project overview and portfolio purposes only.

---

## 🌍 Why Soil Carbon Matters

Soil carbon is a critical indicator of ecosystem health. It supports plant growth, retains water, and captures atmospheric CO₂ — making it vital for sustainable land use and climate change mitigation.

However, traditional soil carbon measurement requires expensive lab testing — making it inaccessible for many farmers, landowners, and researchers.

---

## 💡 Our Solution

**CarbonSense** makes carbon analysis fast, portable, and affordable by turning raw Near-Infrared (NIR) spectral data into usable carbon predictions — no lab needed.

### ✅ Key Features

- Upload raw NIR spectral data (CSV format) collected from a handheld spectrometer
- Receive an instant prediction of soil carbon percentage
- Upload up to 4 files and get the average result
- Clean, responsive interface built with modern web technologies
- Built-in client-side validation and real-time feedback

---

## 🧪 How It Works

1. **Scan Soil Sample**  
   A handheld NIR spectrometer scans the soil sample and collects reflectance data.

2. **Export Data**  
   Data is transferred via Bluetooth to a mobile app and exported as a CSV file.

3. **Upload to CarbonSense**  
   The user uploads 1–4 CSV files to our web platform.

4. **Cloud Processing**  
   Files are stored in **Azure Blob Storage**. A **Flask** backend preprocesses the data by applying smoothing algorithms, interpolation and averaging the data from all uploaded files, and feeds it to a pre-trained **ONNX** model.

5. **Carbon Prediction**  
   The system returns an estimated soil carbon percentage within seconds.

---

## 🛠️ Tech Stack

### Frontend

- [Next.js](https://nextjs.org/)
- [TypeScript](https://www.typescriptlang.org/)
- [Tailwind CSS](https://tailwindcss.com/)

### Backend

- [Python](https://www.python.org/)
- [Flask](https://flask.palletsprojects.com/)
- [ONNX Runtime](https://onnx.ai/)
- [Azure Blob Storage](https://azure.microsoft.com/en-us/products/storage/blobs/)
- Hosted on [Vercel](https://vercel.com/)

---

## 🤖 Machine Learning Model

- **Method:** Partial Least Squares Regression (PLSR)
- **Preprocessing:** Multiplicative Scatter Correction (MSC), Interpolation
- **Wavelength Range:** 950–1650 nm
- **Performance:**
  - R² Score: `0.18`
  - RMSEP: `2.4`
- **Export Format:** ONNX for lightweight deployment

> 📌 *Note: The model is a functional baseline and will benefit from further training and refinement in future iterations.*

---

## 📦 Project Deliverables

- Functional Web Application
- Frontend and Backend (not publicly shared)
- Internal & External Documentation
- Cloud-based CSV Data Storage
- Technical and Test Reports

---

## 🔍 Limitations & Future Improvements

- 🔁 Improved model accuracy with larger datasets and alternate algorithms
- 💾 Downloadable result reports
- 🧭 Session tracking or upload history
- 📊 Visualization of results through charts or plots

---

## 🧠 Lessons Learned

**Things that went well:**
- Smooth deployment via Vercel
- Reliable Azure Blob Storage integration
- Strong team collaboration and planning

**Challenges faced:**
- Limited model accuracy
- Vercel deployment size constraints
- Reformatting and optimizing model and libraries

---

## 👥 Project Team

This project was developed by a team of four students:

- Joel Wohlhauser  
- Yuliia Kruta  
- Samuel Fuentes  
- Sean De Guzman  

---

## 📄 License & Ownership

All rights to the software, source code, and associated deliverables are reserved by the clients: **Gareth Chalmers** and **Iroshaka Cooray**. This project is not open source and may not be reused, distributed, or modified without written permission from the clients or the University of the Sunshine Coast.

---


## 📂 About This Repository

This GitHub repository exists to showcase the **CarbonSense** project outcomes. Due to confidentiality constraints, no code files are included. For a live demonstration, visit:

👉 [https://unisc-carbon-sense.vercel.app](https://unisc-carbon-sense.vercel.app)

---

*Developed as part of the University of the Sunshine Coast ICT Industry Project (2025).*
