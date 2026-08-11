# Muhammad Saqeef Shabbir - IoT Project Architectures 
 
## Project Architecture Diagrams 
 
--- 
 
## 1. ParkSmart & BinWise - Smart City IoT Platform 
 
```mermaid 
graph TD 
    subgraph "Frontend" 
        A[Angular 14+ Web App] --> B[React Native Mobile App] 
    end 
 
    subgraph "Backend (AWS)" 
        B --> C[API Gateway] 
        C --> D[Load Balancer] 
        D --> E[Microservices: Spring Boot/Node.js] 
        E --> F[(PostgreSQL RDS)] 
        E --> G[Redis Cache] 
        E --> H[AWS Lambda Serverless] 
    end 
 
    subgraph "Data Pipeline ^& AI" 
        H --> I[Device Data: IoT Core/Kinesis] 
        I --> J[(S3 Data Lake)] 
        J --> K[ETL: Python/Pandas] 
        K --> L[Training: TensorFlow] 
        L --> M[SageMaker Model Serving] 
        M --> E 
    end 
 
    subgraph "Device Layer" 
        N[Milesight Sensors] --> I 
    end 
 
    subgraph "CI/CD" 
        O[Jenkins/GitHub Actions] --> E & H & A 
    end 
``` 
 
--- 
 
## 2. NFS Ascent - Asset-Based Financing Platform 
 
```mermaid 
graph TD 
    subgraph "Client Applications" 
        A[Angular Web App] --> B[WPF Desktop Client] 
    end 
 
    subgraph "Backend" 
        B --> C[API Gateway/Load Balancer] 
        A --> C 
        C --> D[Web Server: .NET/ASP.NET MVC] 
        D --> E[Business Logic: C#/MVVM] 
        E --> F[(SQL Database)] 
        E --> G[Crystal Reports] 
    end 
 
    subgraph "CI/CD" 
        D & E & F --> H[Git Repository] 
        H --> I[Daily Builds Pipeline] 
    end 
``` 
 
--- 
 
## 3. Sales & Distribution Pro - Retail Management 
 
```mermaid 
graph TD 
    subgraph "Frontend/UI" 
        A[Web Forms: C#/ASP.NET] --> B[Desktop Search Tool: C#] 
    end 
 
    subgraph "Application Server" 
        A --> C[Web Server: .NET Framework] 
        B --> D[Application Logic/Services] 
        C --> D 
        D --> E[(SQL Database)] 
    end 
 
    subgraph "Automation" 
        D --> F[Console App: End-of-Day] 
        F --> G[Auto Reports Generation] 
    end 
 
    subgraph "Deployment" 
        D --> H[Git] 
        H --> I[Bi-Weekly Releases] 
    end 
``` 
 
--- 
 
## 4. NLP Sentiment Analyzer - Freelance Project 
 
```mermaid 
graph TD 
    subgraph "Input Data" 
        A[User Input: Text/Reviews] --> B[Data Ingestion: CSV/API] 
    end 
 
    subgraph "Processing" 
        A & B --> C[Backend: Node.js/Python] 
        C --> D[IBM Watson NLP APIs] 
        D --> E[(Results Database)] 
    end 
 
    subgraph "Output" 
        E --> F[Dashboard: Angular/React] 
        F --> G[End Users: Feedback/Analysis] 
    end 
```

--- 

## 5. ComfyUI with ImaginArt with custom nodes - Open Source Project 
 
```mermaid 
graph TB
    subgraph User_Interface["🎨 User Interface Layer"]
        Browser[Web Browser<br>http://127.0.0.1:8188]
        CLI[Command Line Interface<br>python main.py --listen --cpu]
    end

    subgraph ComfyUI_Core["⚙️ ComfyUI Core Engine"]
        Server[ComfyUI Server<br>main.py]
        Router[Node Router<br>execution.py]
        Workflow[Workflow Manager<br>Queues & Execution]
    end

    subgraph Custom_Nodes["🔌 Custom Nodes Layer"]
        Manager[ComfyUI-Manager<br>Node Management]
        VideoHelper[VideoHelperSuite<br>Video Generation]
        ControlNet[ComfyUI-ControlNet<br>Pose/Edge Control]
        IPAdapter[IPAdapter_plus<br>Face/Character Consistency]
        ImpactPack[Impact-Pack<br>Upscaling & Processing]
    end

    subgraph Models["🧠 AI Models Layer"]
        SDXL[SDXL Base<br>Image Generation<br>~6.94 GB]
        Refiner[SDXL Refiner<br>Image Refinement<br>~6.07 GB]
        SVD[SVD-XT<br>Video Generation<br>~7.87 GB]
        Canny[ControlNet Canny<br>Edge Detection<br>~2.55 GB]
    end

    subgraph Processing["⚡ Processing Layer"]
        CPU[CPU Mode<br>Fallback]
        Attention[Attention Module<br>comfy_kitchen]
        VAE[VAE Decoder<br>Image/Video Decoding]
    end

    subgraph Storage["💾 Storage Layer"]
        Input[(Input Images<br>/input/)]
        Output[(Generated Outputs<br>/output/)]
        ModelsFolder[(Model Weights<br>/models/)]
        UserData[(User Settings<br>/user/)]
    end

    Browser --> Server
    CLI --> Server
    Server --> Router
    Router --> Workflow
    Workflow --> Custom_Nodes
    Custom_Nodes --> Models
    Models --> Processing
    Processing --> Storage
    Storage --> Output
    ModelsFolder --> Models
    Input --> Processing
    Output --> Browser
```
--- 
 
## How to View These Diagrams 
 
1. On **GitHub**, these diagrams render automatically in the README 
2. In **VS Code**, install the "Markdown Preview Mermaid Support" extension 
3. Use **https://mermaid.live** to edit and export as images 
 
## About the Developer 
 
**Muhammad Saqeef Shabbir** 
- Senior Full Stack Engineer with 7+ years experience 
- Expertise: Angular, React, Spring Boot, Node.js, AWS, Azure 
- LinkedIn: [https://www.linkedin.com/in/muhammad-saqeef-shabbir-779668b3/](https://linkedin.com) 
- Portfolio: [https://portfolio-three-sepia-64.vercel.app/](https://portfolio-three-sepia-64.vercel.app) 
