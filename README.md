# Price-radar
This project is about AI-powered competitive intelligence for Indian e-commerce sellers. Analyses competitor pricing, customer reviews, and market signals to decode strategy and recommend actions.

# 🚀 PriceRadar
India E-Commerce Price Intelligence Dashboard


PriceRadar is an E-commerce price intelligence dashboard that compares product prices, discounts, ratings, and value scores across five major Indian online marketplaces:

🛒 Amazon

🛒 Flipkart

🛒 Myntra

🛒 Snapdeal

The project demonstrates the complete data science pipeline, from data collection to machine learning to an interactive dashboard.
Built for Datathon 2026.

# 📌 Problem Statement
Online shoppers often need to manually check multiple platforms to find the best deal.

Example scenario:
A user wants to buy a laptop or clothing item.

They must visit:
Amazon
Flipkart
Myntra
Snapdeal

This process is time-consuming and inefficient.

# 💡 Solution – PriceRadar
PriceRadar provides:

✅ Cross-platform price comparison

✅ Unified product categories

✅ Value score for best deals

✅ AI-powered buying insights

✅ Interactive data dashboard
The system aggregates product data from five marketplaces and provides data-driven shopping intelligence.

# 📊 Dataset
Datasets were collected from Kaggle public repositories.

Platform

Dataset

Approx Rows

Amazon
amazon-sales-dataset
~1,465
Flipkart
flipkart-products
~20,000
Myntra
myntra-products
~20,000
Snapdeal
flipkart-ecommerce-dataset
~5,000

# ⚙️ Feature Engineering
Several new analytical features were generated.

Feature

Description

value_score

Combines price, rating, discount

savings_amount

MRP − selling price

discount_tier

Low / Medium / High / Mega

review_power

rating × log(rating_count + 1)

price_norm

normalized price is_high_rated 
rating ≥ 4.0 is_deep_discount 
discount ≥ 40%

These features help identify the best value products across platforms.

# 🧠 Category Normalization
Different platforms use different category naming systems.

PriceRadar maps them into 10 unified super-categories:

Electronics

Fashion – Men

Fashion – Women

Footwear

Home & Kitchen

Beauty & Personal Care

Sports & Fitness

Books & Stationery

Bags & Accessories

Toys & Baby

This enables fair cross-platform comparison.

# 🔄 Data Pipeline
The entire pipeline runs inside Google Colab.
Pipeline Steps

1️⃣ Data Collection (Kaggle API)

2️⃣ Data Standardization
Unified column schema across platforms

3️⃣ Dataset Merge
All platforms merged into one dataset

4️⃣ Data Cleaning
Remove currency symbols
Convert data types
Handle missing values

5️⃣ Feature Engineering

6️⃣ Exploratory Data Analysis

7️⃣ Machine Learning Models

8️⃣ Export final dataset

# Output file:
Copy code

bazaariq_5platform_clean.csv

# 🤖 Machine Learning Models

Model

Algorithm

Purpose

Platform Classifier

Random Forest

Detect pricing patterns

Price Predictor

Random Forest Regressor

Predict expected price

Rating Classifier

Gradient Boosting

Predict high-rated products

# 📈 PriceRadar Dashboard
The dashboard is built using:

HTML

CSS

JavaScript

Chart.js

It is a single standalone HTML application.

No backend or installation required.

# 🖥 Dashboard Features
# 📊 Platform Comparison
Users select a category to view:

Minimum price

Average price

Maximum price

Discount percentage

Ratings

Value score

Includes multiple visual charts.

# 🔎 Product Explorer
Users can:

Search products

Filter by platform

Filter by price

Filter by rating

Sort by value score

View product insights


# 🧪 Demo Mode
The dashboard includes 98 embedded sample products.
This allows:

✔ Instant dashboard loading

✔ No dataset upload required

Users can also upload their own dataset using:

Copy code

# Load Your CSV
📂 Project Structure
Copy code

# PriceRadar
│

├── PriceRadar.html

├── BazaarIQ_5Platform_Pipeline.ipynb

├── BazaarIQ_Real_Kaggle_Pipeline.ipynb

├── bazaariq_5platform_clean.csv

├── BazaarIQ_Abstract.docx

└── README.md

# ▶️ How to Run
Run the Dashboard

Simply open:

Copy code

# PriceRadar.html
in any modern browser:

Chrome

Edge

Firefox

No installation required.

Run the Data Pipeline

Open the notebook:

Copy code

# BazaarIQ_5Platform_Pipeline.ipynb
Steps:

Upload kaggle.json

Run all cells

Dataset downloads automatically

Output CSV is generated

Load the CSV into the dashboard.

# 🤖 AI Buying Insights (Optional)
PriceRadar supports AI-generated buying insights using Claude API.

To enable:

1️⃣ Get API key from Anthropic

2️⃣ Add the key in PriceRadar.html
Javascript

Copy code

const ANTHROPIC_KEY = "your_api_key";

If no key is provided, the dashboard uses rule-based insights.

# ❓ Frequently Asked Questions

Why compare categories instead of products?
Different datasets do not share common product IDs, so category-level comparison ensures statistical fairness.

What is Value Score?

A composite metric:
Copy code

Value Score = (rating / 5) × (discount / 100) × (1 / price_norm)
Higher value score indicates better price-quality balance.
Is this production ready?
This is a prototype.

Future improvements may include:

Real-time product scraping

Backend API

Mobile application

User accounts

Live price tracking


# 🏆 Project Information

Field

Details

Project Name

PriceRadar

Event

Datathon 2026

Domain

E-Commerce Intelligence

Tech Stack

Python, Pandas, Scikit-learn, HTML, CSS, JavaScript

Visualization

Chart.js

Data Source

Kaggle

Dashboard

Standalone HTML
