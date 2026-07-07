# 📚 Jyoti-ctr's Project Portfolio

A comprehensive overview of all projects with detailed documentation, tech stacks, build processes, and key objectives.

---

## 📑 Table of Contents
1. [Campus Event System](#1-campus-event-system)
2. [Customer Insights & Spending Score Prediction](#2-customer-insights--spending-score-prediction)
3. [FinanceFlow](#3-financeflow)
4. [Ecommerce](#4-ecommerce)
5. [AI-Powered Multimodal Virtual Mouse](#5-ai-powered-multimodal-virtual-mouse)
6. [Other Projects](#6-other-projects)

---

## 1. Campus Event System

### 📌 Project Overview
A full-stack college event management platform that enables students and organizations to discover, register, and organize campus events. Features a comprehensive admin dashboard for event management.

### 🎯 Aim
- Provide a centralized platform for campus event discovery and management
- Enable seamless event registration and user engagement
- Offer analytics through statistics dashboard
- Create role-based access for different user types (admin, regular users)

### 🛠️ Tech Stack
**Frontend:**
- React 18 with TypeScript
- Vite (Build tool)
- Tailwind CSS (Styling)
- shadcn/ui (Component library)
- Lucide React (Icons)

**Backend:**
- Flask (Python)
- SQLite (Database)

### 📐 Project Structure
```
campus-event-system/
├── college_event/
│   ├── app/                    # React Frontend
│   │   ├── src/
│   │   │   ├── sections/       # Page sections (Hero, Events, Categories)
│   │   │   ├── services/       # API service layer
│   │   │   ├── types/          # TypeScript definitions
│   │   │   ├── App.tsx
│   │   │   └── index.css
│   │   └── dist/               # Built files
│   ├── backend/                # Flask Backend
│   │   ├── app.py              # Main Flask app
│   │   ├── models.py           # Database models
│   │   ├── seed_data.py        # Sample data
│   │   └── requirements.txt
│   └── start.sh
```

### 🏗️ How to Build - Step by Step

**Backend Setup:**
```bash
cd backend
pip install -r requirements.txt
python3 seed_data.py
python3 app.py
# Backend runs on http://localhost:5000
```

**Frontend Setup:**
```bash
cd app
npm install
npm run dev
# Frontend runs on http://localhost:5173
```

**Production Build:**
```bash
cd app
npm run build
# Output in app/dist/
```

### 🔑 Key Features
- **Event Discovery**: Browse and filter events by category
- **Event Submission**: User-friendly form for event creation
- **Registration System**: Track attendee registrations
- **Statistics Dashboard**: Animated counters showing platform metrics
- **Responsive Design**: Mobile-optimized interface
- **Role-Based Auth**: Admin and user access levels

### 💾 Database Schema
- **Event**: Title, description, date/time, location, category, capacity tracking
- **User**: Student ID, name, email, major, year
- **Registration**: Event-user mapping with status tracking
- **Category**: Event categorization (Music, Career, Arts, Technology, Sports, Culture)

### 🎨 Design System
- Primary Orange: `#ff8a01`
- Secondary Green: `#314c53`
- Typography: Montserrat (headings), Inter (body)

### 📊 API Endpoints
- `GET/POST /api/events` - Event management
- `GET /api/categories` - Category listing
- `GET/POST /api/users` - User management
- `GET/POST/DELETE /api/registrations` - Registration handling
- `GET /api/stats` - Platform statistics

---

## 2. Customer Insights & Spending Score Prediction

### 📌 Project Overview
An end-to-end machine learning pipeline for customer segmentation and spending behavior prediction. Uses advanced algorithms to identify customer personas and predict spending patterns with high accuracy.

### 🎯 Aim
- Segment customers into distinct personas based on income and spending behavior
- Predict customer spending scores (1-100) for targeted marketing
- Provide business insights for customer targeting strategies
- Achieve high accuracy in prediction models

### 🛠️ Tech Stack
- **Language**: Python 3.10
- **ML Libraries**: XGBoost, scikit-learn
- **Clustering**: K-Means++
- **Data Processing**: Pandas, NumPy
- **Visualization**: Matplotlib

### 📊 Project Structure
```
Customer-Insights-Spending-Score-Prediction/
├── src/
│   ├── preprocess.py    # Data preprocessing
│   ├── cluster.py       # K-Means++ clustering
│   └── predict.py       # XGBoost prediction
├── requirements.txt
└── app.py
```

### 🏗️ How to Build - Step by Step

**1. Clone & Setup Environment:**
```bash
git clone https://github.com/Jyoti-ctr/Customer-Insights-Spending-Score-Prediction.git
cd Customer-Insights-Spending-Score-Prediction
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

**2. Install Dependencies:**
```bash
pip install -r requirements.txt
```

**3. Run Pipeline Stages:**
```bash
# Preprocess data
python src/preprocess.py

# Perform clustering
python src/cluster.py

# Predict spending scores
python src/predict.py

# Or run full pipeline
python app.py
```

### 📈 Model Performance
- **Accuracy**: 84.4% R² score
- **Clustering**: 5 distinct customer personas identified

### 💡 Business Insights
**Cluster 0**: High Income / Low Spenders
- Target with savings-based luxury ads
- Premium quality, long-lasting products

**Cluster 2**: High Income / High Spenders
- VIP customer segment
- Loyalty rewards, exclusive access

### 🔄 Pipeline Workflow
1. Data Preprocessing: Cleaning, normalization, feature engineering
2. Clustering: K-Means++ segmentation into 5 clusters
3. Feature Analysis: Identify key spending drivers
4. XGBoost Training: Predict spending scores
5. Model Evaluation: R² score calculation and validation

---

## 3. FinanceFlow

### 📌 Project Overview
A modern full-stack personal finance management application. Users can track income/expenses, manage categories, and visualize spending patterns through interactive dashboards and reports.

### 🎯 Aim
- Simplify personal finance tracking and management
- Provide clear visualization of income and expense patterns
- Enable users to create custom categories for better organization
- Generate insightful financial reports for better decision-making
- Ensure secure financial data with JWT authentication

### 🛠️ Tech Stack
**Backend:**
- FastAPI (Python framework)
- SQLAlchemy (ORM)
- SQLite (Database)
- Pydantic (Data validation)
- JWT (Authentication)

**Frontend:**
- React 18 (UI library)
- Recharts (Data visualization)
- Axios (HTTP client)

### 📐 Project Structure
```
financeflow/
├── backend/
│   ├── main.py                 # FastAPI main app
│   ├── models.py               # SQLAlchemy models
│   ├── requirements.txt
│   └── .env                    # Environment variables
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   └── App.jsx
│   ├── package.json
│   └── public/
└── README.md
```

### 🏗️ How to Build - Step by Step

**Backend Setup (Terminal 1):**
```bash
cd backend

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Create .env file
echo "SECRET_KEY=your-secret-key-here" > .env
echo "DATABASE_URL=sqlite:///./finance.db" >> .env

# Run backend
uvicorn main:app --reload
# Backend runs on http://localhost:8000
```

**Frontend Setup (Terminal 2):**
```bash
cd frontend

# Install dependencies
npm install

# Start development server
npm start
# Frontend runs on http://localhost:3000
```

### 🔑 Key Features
1. **User Authentication**: Secure registration and login with JWT tokens
2. **Transaction Management**: Add, edit, delete income and expense entries
3. **Category Management**: Create custom categories for better organization
4. **Dashboard**: Overview of financial data with key metrics
5. **Reports**: Detailed spending analysis and visualization
6. **Data Visualization**: Interactive charts using Recharts

### 📱 User Workflow
1. Register new account
2. Login with credentials
3. Create income/expense categories
4. Add transactions
5. View dashboard for financial overview
6. Check reports for spending patterns

### 🔐 Security
- JWT-based authentication
- Secure password storage
- User-specific data isolation

### 📊 Database Models
- User: Authentication and profile
- Category: Transaction categories
- Transaction: Income/expense records
- Dashboard: Aggregated financial data

---

## 4. Ecommerce

### 📌 Project Overview
A modern ecommerce application built with React frontend and Node.js backend. Enables users to browse products, manage cart, and complete transactions.

### 🎯 Aim
- Create a user-friendly ecommerce platform
- Implement product browsing and search functionality
- Enable shopping cart and checkout process
- Build scalable backend API architecture
- Provide responsive mobile and desktop experience

### 🛠️ Tech Stack
**Frontend:**
- React (UI framework)
- Vite (Build tool)
- JavaScript/JSX

**Backend:**
- Node.js (Runtime)
- Express (Web framework)

### 📐 Project Structure
```
Ecommerce/
├── ecommerce-react/
│   ├── ecomerce-project/     # React Frontend
│   │   ├── src/
│   │   ├── public/
│   │   └── package.json
│   └── ecommerce-backend/    # Node.js Backend
│       ├── server.js
│       ├── routes/
│       ├── models/
│       └── package.json
```

### 🏗️ How to Build - Step by Step

**Backend Setup:**
```bash
cd ecommerce-react/ecommerce-backend

# Prerequisites: Node.js 22+

# Install dependencies
npm install

# Start development server
npm run dev
```

**Frontend Setup:**
```bash
cd ecommerce-react/ecomerce-project

# Install dependencies
npm install

# Start development server
npm run dev
```

### 🔑 Key Features
- Product catalog browsing
- Shopping cart management
- Order processing
- Responsive design

---

## 5. AI-Powered Multimodal Virtual Mouse

### 📌 Project Overview
An innovative application using AI and computer vision to control a virtual mouse using hand gestures and voice commands. Enables hands-free computer interaction.

### 🎯 Aim
- Create a hands-free computer interface using AI
- Implement multimodal input (gesture + voice)
- Provide accessibility features for users
- Demonstrate advanced computer vision capabilities
- Enable intuitive human-computer interaction

### 🛠️ Tech Stack
- **Language**: Python
- **Computer Vision**: OpenCV, MediaPipe
- **AI/ML**: TensorFlow/PyTorch
- **Voice Processing**: Speech recognition libraries

### 🎯 Key Features
- Hand gesture recognition
- Voice command processing
- Virtual mouse cursor control
- Gesture-based click/drag operations

---

## 6. Other Projects

### 6.1 AssessmentRound_1
**Language**: Python
**Description**: Assessment or evaluation project
**Repository**: https://github.com/Jyoti-ctr/AssesmentRound_1

### 6.2 CommBank-Server
**Language**: Java/Python
**Description**: Operations in simulated job environment for CommBank
**Repository**: https://github.com/Jyoti-ctr/CommBank-Server

### 6.3 devp_10
**Language**: Java
**Repository**: https://github.com/Jyoti-ctr/devp_10

### 6.4 helloworld-app
**Language**: Java
**Repository**: https://github.com/Jyoti-ctr/helloworld-app

### 6.5 myapp & myapp-demo
**Language**: Java
**Repository**: https://github.com/Jyoti-ctr/myapp
**Repository**: https://github.com/Jyoti-ctr/myapp-demo

### 6.6 dheecodinglab
**Language**: HTML
**Repository**: https://github.com/Jyoti-ctr/dheecodinglab

### 6.7 personalDairy
**Language**: HTML/CSS/JavaScript
**Repository**: https://github.com/Jyoti-ctr/personalDairy

### 6.8 PavanXDCL_Web
**Language**: CSS/HTML
**Repository**: https://github.com/Jyoti-ctr/PavanXDCL_Web

### 6.9 Student_record_management
**Language**: HTML/CSS/JavaScript
**Repository**: https://github.com/Jyoti-ctr/Student_record_management

### 6.10 Youtube
**Language**: HTML/CSS/JavaScript
**Repository**: https://github.com/Jyoti-ctr/Youtube

### 6.11 pavanxdcl
**Repository**: https://github.com/Jyoti-ctr/pavanxdcl

---

## 📊 Skills & Technologies Overview

### **Languages**
- Python (ML, Web Backend)
- JavaScript/TypeScript (Frontend)
- Java (Backend, Learning)
- HTML/CSS (Web)

### **Frontend Technologies**
- React 18
- TypeScript
- Tailwind CSS
- Vite
- shadcn/ui

### **Backend Technologies**
- FastAPI
- Flask
- Node.js
- SQLAlchemy
- SQLite

### **Machine Learning & AI**
- XGBoost
- K-Means++
- scikit-learn
- Computer Vision (OpenCV, MediaPipe)

### **Development Tools**
- Git/GitHub
- npm
- pip
- Docker (potential)

---

## 🎓 Learning Progression

1. **Foundation**: Java basics (helloworld-app, myapp)
2. **Web Development**: HTML/CSS/JS projects
3. **Full-Stack Development**: React + Node/Python backends
4. **Data Science**: ML pipelines and predictions
5. **Advanced**: Multimodal AI applications

---

## 🚀 Getting Started with Your Projects

### Clone All Repos
```bash
git clone https://github.com/Jyoti-ctr/campus-event-system.git
git clone https://github.com/Jyoti-ctr/Customer-Insights-Spending-Score-Prediction.git
git clone https://github.com/Jyoti-ctr/financeflow.git
git clone https://github.com/Jyoti-ctr/Ecommerce.git
```

### Common Development Workflow
1. Clone repository
2. Install dependencies (npm install / pip install -r requirements.txt)
3. Setup environment variables if needed
4. Run development server
5. Make changes and test
6. Commit and push to GitHub

---

## 📝 Notes

- Most projects include both backend and frontend components
- Full-stack projects require running multiple servers simultaneously
- Database seeds are available for quick setup
- All projects are documented with READMEs in their repositories

---

**Last Updated**: 2024
**Total Projects**: 18 repositories
**Primary Focus**: Full-Stack Development, Machine Learning, Web Applications

