<div align="center">
  <br />      <img src="./public/drug_research.jpg" alt="ProteinBind Project Banner">
  
  <br />

  <div>
    <img src="https://img.shields.io/badge/-TypeScript-black?style=for-the-badge&logoColor=white&logo=typescript&color=3178C6" alt="typescript" />
    <img src="https://img.shields.io/badge/-Next_JS-black?style=for-the-badge&logoColor=white&logo=nextdotjs&color=000000" alt="nextdotjs" />
    <img src="https://img.shields.io/badge/-Tailwind_CSS-black?style=for-the-badge&logoColor=white&logo=tailwindcss&color=06B6D4" alt="tailwindcss" />
    <img src="https://img.shields.io/badge/-NVIDIA_NIM-black?style=for-the-badge&logoColor=white&logo=nvidia&color=76B900" alt="nvidia-neMo" />
  </div>

  <h3 align="center">ProteinBind</h3>

   <div align="center">
     A comprehensive protein structure prediction and analysis platform.
    </div>
</div>

## 📋 <a name="table">Table of Contents</a>

1. 🤖 [Introduction](#introduction)
2. ⚙️ [Tech Stack](#tech-stack)
3. 🔋 [Features](#features)
4. 🤸 [Quick Start](#quick-start)
5. 🧬 [Protein Data Processing](#protein-data)
6. 🚀 [More](#more)
7. 🧪 [NVIDIA API Test Script](#nvidia-api-test-script)

## <a name="introduction">🤖 Introduction</a>

**ProteinBind** is a drug discovery and protein-binding prediction tool built with the latest in machine learning and natural language processing (NLP) technology. Powered by NVIDIA NIM and protein structure prediction models, this project enables users to simulate molecular interactions and predict protein structures.

The platform is designed to help researchers accelerate drug discovery by leveraging cutting-edge AI models for protein folding, docking, and molecular dynamics.

## <a name="tech-stack">⚙️ Tech Stack</a>

- **Next.js**
- **TypeScript**
- **NVIDIA** (for protein structure prediction)
- **Tailwind CSS**
- **React Chart.js** (for visualizing protein data)

## <a name="features">🔋 Features</a>

👉 **Protein Structure Prediction**: Predicts 2D protein structures using NVIDIA models.

👉 **Collaborative Research**: Researches can create groups and colloborate with other research online

👉 **Responsive Design**: Ensures seamless experience across all devices, from desktops to mobile.

## <a name="quick-start">🤸 Quick Start</a>

Follow these steps to set up the project locally on your machine.

### **Prerequisites**

Make sure you have the following installed on your machine:

- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/en)
- [npm](https://www.npmjs.com/) (Node Package Manager)

### **Cloning the Repository**

```bash
git clone https://github.com/Mayankdaya/ProteinBind.git
cd proteinbind
```

### **Installation**

Install the project dependencies using npm:

```bash
npm install
```

### **Set Up Environment Variables**

Create a new file named `.env` in the root of your project and add the following content:

```env
NEXT_PUBLIC_NVIDIA_API_KEY=your-nvidia-api-key

ABLY_API_KEY='your-ably-api-key'

MONGODB_URL='your-mongodb-url'

NEXT_PUBLIC_API_BASE_URL=http://localhost:3000

RESEND_KEY='your-resend-api-key'
```

### **Running the Project**

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to view the project.

## <a name="protein-data">🧬 Protein Data Processing</a>

This section covers the protein data processing pipeline, including loading protein structure files (e.g., PDB format), performing molecular docking simulations, and visualizing the results.

### **Protein Structure Input**

Users can upload PDB files for protein structures, which will then be processed by NVIDIA NeMo's protein-folding models.

### **Docking Simulation**

Using molecular docking algorithms, the system predicts how small molecules (such as drug candidates) bind to protein targets.

## <a name="more">🚀 More</a>

Stay tuned for more updates and features! Feel free to contribute to the repository by opening pull requests.

## <a name="nvidia-api-test-script">🧪 NVIDIA API Test Script</a>

This script tests the NVIDIA Molecular Optimization API.

### **Prerequisites**

- curl
- bash
- Valid NVIDIA API key
- A terminal/command prompt

### **Testing Instructions**

1. Set your API key in your environment:
```bash
# For Windows
set API_KEY_REQUIRED_IF_EXECUTING_OUTSIDE_NGC=your_api_key

# For Linux/Mac
export API_KEY_REQUIRED_IF_EXECUTING_OUTSIDE_NGC=your_api_key
```

2. Run the test command:
```bash
curl -X POST "https://health.api.nvidia.com/v1/biology/nvidia/molmim/generate" \
-H "Authorization: Bearer $API_KEY_REQUIRED_IF_EXECUTING_OUTSIDE_NGC" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-d '{
  "algorithm": "CMA-ES",
  "num_molecules": 30,
  "property_name": "QED",
  "minimize": false,
  "min_similarity": 0.3,
  "particles": 30,
  "iterations": 10,
  "smi": "[H][C@@]12Cc3c[nH]c4cccc(C1=C[C@H](NC(=O)N(CC)CC)CN2C)c34"
}'
```

### **Expected Response**
If successful, you should receive a JSON response containing:
- Generated molecules
- Optimization scores
- Similarity metrics

### **Troubleshooting**
- If you get a 401 error, check your API key
- If you get a timeout, try reducing the number of molecules
- For connection issues, verify your internet connection

## 📞 **Contact & Support**

If you have any questions or need support, please open an issue in the GitHub repository.
