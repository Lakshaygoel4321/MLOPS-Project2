# MLOPs-Production-Ready-Machine-Learning-Project 🚀  

This repository showcases a production-ready MLOps pipeline designed to deploy and maintain machine learning models efficiently. The project leverages powerful tools and best practices, ensuring seamless model deployment and monitoring in a real-world environment.

---

## 📺 YouTube Playlist  
Follow the complete implementation and detailed explanations:  
[Watch on YouTube](https://youtube.com/playlist?list=PLkz_y24mlSJZvJOj1UXiJPVRQrNFdNEXX&si=FRFLpnve9MS6Rii9)  

---

## 🛠 Tools & Technologies  
This project utilizes the following tools:  
- **Anaconda**: [Download Here](https://www.anaconda.com/)  
- **Visual Studio Code**: [Download Here](https://code.visualstudio.com/download)  
- **Git**: [Download Here](https://git-scm.com/)  
- **Flowchart Design (Whimsical)**: [Explore Here](https://whimsical.com/)  
- **MLOps Tool (Evidently AI)**: [Learn More](https://www.evidentlyai.com/)  
- **MongoDB**: [Login Here](https://account.mongodb.com/account/login)  

---

## 📊 Dataset  
The project uses the EasyVisa dataset available on Kaggle:  
[Download Dataset](https://www.kaggle.com/datasets/moro23/easyvisa-dataset)

---

## ⚙️ Workflow  
The MLOps pipeline is organized into the following modules:  
- **Constants**: Centralized configuration and constants.  
- **Entity**: Data structures and schema definitions.  
- **Components**: Core ML pipeline components, including data ingestion, transformation, and model training.  
- **Pipeline**: Orchestrates the end-to-end workflow.  
- **Main File**: Entry point to run the pipeline.  

---

## 🖥 How to Run the Project?  
Follow these steps to set up and run the project:  

### Step 1: Clone the Repository  
```bash
git clone <repository-url>
cd MLOPS-Project2
```

### Step 2: Create and Activate Conda Environment  
```bash
conda create -n visa python=3.8 -y
conda activate visa
```

### Step 3: Install Required Dependencies  
```bash
pip install -r requirements.txt
```

### Step 4: Export Environment Variables  
Make sure to replace `<username>`, `<password>`, and other placeholders with your actual credentials:  
```bash
export MONGODB_URL="mongodb+srv://<username>:<password>...."
export AWS_ACCESS_KEY_ID=<AWS_ACCESS_KEY_ID>
export AWS_SECRET_ACCESS_KEY=<AWS_SECRET_ACCESS_KEY>
```

### Step 5: Run the Pipeline  
```bash
python main.py
```

---

## 📂 Git Commands  
Use the following commands to manage your repository:  
```bash
git add .
git commit -m "Updated"
git push origin main
```

---

## 🚀 AWS-CICD-Deployment-with-Github-Actions  
Automate the deployment process using GitHub Actions integrated with AWS services.  

### 1. **Login to AWS Console**  
- Create an IAM user with the following access:  
  - **EC2 Access**: For launching virtual machines.  
  - **ECR Access**: Elastic Container Registry to store Docker images.  

### 2. **Deployment Workflow**  
1. **Build Docker Image**: Create a Docker image of the source code.  
2. **Push to ECR**: Store the Docker image in AWS ECR.  
3. **Launch EC2**: Start an EC2 instance.  
4. **Pull Image from ECR**: Fetch the image from ECR in EC2.  
5. **Run Docker Image**: Deploy the containerized application on EC2.  

### 3. **Required IAM Policies**  
- `AmazonEC2ContainerRegistryFullAccess`  
- `AmazonEC2FullAccess`  

### 4. **Create ECR Repository**  
Save the URI:  
```
315865595366.dkr.ecr.us-east-1.amazonaws.com/visarepo
```

### 5. **Create EC2 Machine (Ubuntu) & Install Docker**  
```bash
sudo apt-get update -y
sudo apt-get upgrade
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker ubuntu
newgrp docker
```

### 6. **Configure EC2 as Self-Hosted Runner**  
Go to **GitHub > Settings > Actions > Runner > New Self Hosted Runner**, choose OS, and run the provided commands.

### 7. **Setup GitHub Secrets**  
- `AWS_ACCESS_KEY_ID`  
- `AWS_SECRET_ACCESS_KEY`  
- `AWS_DEFAULT_REGION`  
- `ECR_REPO`  

---

## 🎯 Key Features  
- End-to-end MLOps pipeline with automated CI/CD using GitHub Actions.  
- Seamless deployment on AWS with EC2 and ECR integration.  
- Scalable and maintainable architecture using modular components.  
- Real-time monitoring and analytics with Evidently AI.  

---

## 🤝 Contribution  
Contributions are welcome! Feel free to submit a pull request or open an issue.  

---

## 📄 License  
This project is licensed under the MIT License.  

---

This README.md is crafted to attract recruiters and users by clearly explaining the project purpose, technology stack, workflow, and deployment process. You can directly add this to your GitHub repository. If you want any modifications or additional sections, let me know! 🚀
