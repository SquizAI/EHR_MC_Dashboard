<div align="center">

# 🏥 EHR MC Dashboard 📊

[![GitHub stars](https://img.shields.io/github/stars/SquizAI/EHR_MC_Dashboard?style=for-the-badge)](https://github.com/SquizAI/EHR_MC_Dashboard/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/SquizAI/EHR_MC_Dashboard?style=for-the-badge)](https://github.com/SquizAI/EHR_MC_Dashboard/network/members)
[![GitHub issues](https://img.shields.io/github/issues/SquizAI/EHR_MC_Dashboard?style=for-the-badge)](https://github.com/SquizAI/EHR_MC_Dashboard/issues)
[![GitHub license](https://img.shields.io/github/license/SquizAI/EHR_MC_Dashboard?style=for-the-badge)](https://github.com/SquizAI/EHR_MC_Dashboard/blob/main/LICENSE)

<p align="center">
  <img src="https://raw.githubusercontent.com/SquizAI/EHR_MC_Dashboard/main/public/dashboard-preview.gif" alt="Dashboard Preview" width="80%">
</p>

_A powerful dashboard for healthcare analytics, with AI-driven insights for Electronic Health Records and Medical Conversations_

[Features](#-features) • [Demo](#-live-demo) • [Technology](#-technology) • [Getting Started](#-getting-started) • [Usage](#-usage) • [Roadmap](#-roadmap) • [Contributing](#-contributing) • [License](#-license)

</div>

## 🌟 Features

<div align="center">
<table>
<tr>
<td width="50%">

### 📋 Data Integration
- Upload EHR/conversation data from CSV files
- Automatic mapping of funnel stages
- Support for various healthcare data formats
- Smart data sampling for large datasets

### 🤖 AI-Powered Analysis
- OpenAI-driven insights generation
- Automatic anomaly detection
- Pattern recognition in patient journeys
- Personalized recommendations

</td>
<td width="50%">

### 📊 Interactive Visualizations
- Conversion funnel analysis
- Channel performance comparison
- Treatment efficacy metrics
- Patient segment analysis

### 📱 Modern UI/UX
- Responsive Material UI design
- Dark/light theme support
- Customizable dashboard layouts
- Mobile-optimized views

</td>
</tr>
</table>
</div>

<p align="center">
  <img src="https://raw.githubusercontent.com/SquizAI/EHR_MC_Dashboard/main/public/features-showcase.png" alt="Features Showcase" width="90%">
</p>

## 🚀 Live Demo

Explore the dashboard with sample data: [EHR MC Dashboard Demo](https://ehr-mc-dashboard.netlify.app)

## 🔧 Technology

<div align="center">

[![React](https://img.shields.io/badge/React-18-61DAFB?style=flat-square&logo=react&logoColor=white)](https://reactjs.org/)
[![Vite](https://img.shields.io/badge/Vite-4-646CFF?style=flat-square&logo=vite&logoColor=white)](https://vitejs.dev/)
[![Material UI](https://img.shields.io/badge/MUI-5-0081CB?style=flat-square&logo=mui&logoColor=white)](https://mui.com/)
[![Chart.js](https://img.shields.io/badge/Chart.js-4-FF6384?style=flat-square&logo=chart.js&logoColor=white)](https://www.chartjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-16+-339933?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-4-000000?style=flat-square&logo=express&logoColor=white)](https://expressjs.com/)
[![OpenAI](https://img.shields.io/badge/OpenAI_API-GPT--4-412991?style=flat-square&logo=openai&logoColor=white)](https://openai.com/)

</div>

### Architecture

```mermaid
graph TD
    A[Client Browser] -->|HTTP Requests| B[React Frontend]
    B -->|API Calls| C[Node.js Backend]
    C -->|CSV Processing| D[Data Parser]
    C -->|AI Analysis| E[OpenAI API]
    D -->|Processed Data| F[Dashboard Visualizations]
    E -->|Insights & Metrics| F
    F -->|UI Rendering| B
```

## 📦 Getting Started

### Prerequisites

- Node.js (v16 or higher)
- OpenAI API Key

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/SquizAI/EHR_MC_Dashboard.git
   cd EHR_MC_Dashboard
   ```

2. **Install frontend dependencies**
   ```bash
   npm install
   ```

3. **Install backend dependencies**
   ```bash
   cd server
   npm install
   cd ..
   ```

4. **Set up environment variables**
   ```bash
   cp .env.example .env
   ```
   Edit `.env` file and add your OpenAI API key:
   ```
   OPENAI_API_KEY=your_api_key_here
   ```

### Running the Application

1. **Start the backend server**
   ```bash
   npm run server
   ```

2. **Start the frontend development server**
   ```bash
   npm run dev
   ```

3. **Open your browser**
   Navigate to: http://localhost:5173

## 📈 Usage

<div align="center">
  <img src="https://raw.githubusercontent.com/SquizAI/EHR_MC_Dashboard/main/public/workflow.png" alt="Dashboard Workflow" width="80%">
</div>

1. **Upload Data**: Import your healthcare data in CSV format
2. **Review Data**: Verify the uploaded information in the preview table
3. **Generate Insights**: Click 'Generate Insights' to analyze data with AI
4. **Explore Metrics**: Navigate through various dashboard components:
   - Conversion Funnel Analysis
   - Channel Performance
   - Patient Demographics
   - Treatment Efficiency
5. **Export & Share**: Download reports or share insights with your team

### Data Format

The dashboard works best with CSV files containing these fields:

| Field | Description | Example |
|-------|-------------|--------|
| `patient_id` | Unique identifier | P12345 |
| `stage` | Patient funnel stage | Awareness, Consideration, Decision |
| `source` | Acquisition channel | Referral, Website, Insurance |
| `timestamp` | Event date/time | 2023-04-15T14:30:00Z |
| `treatment` | Treatment type | Consultation, Procedure, Follow-up |
| `outcome` | Treatment result | Completed, Referred, Cancelled |

<details>
<summary>Show sample CSV format</summary>

```csv
patient_id,stage,source,timestamp,treatment,outcome
P12345,Awareness,Website,2023-04-15T14:30:00Z,Consultation,Completed
P12346,Consideration,Referral,2023-04-16T09:15:00Z,Procedure,Completed
P12347,Decision,Insurance,2023-04-17T11:00:00Z,Follow-up,Cancelled
```
</details>

## 🗺️ Roadmap

- [ ] **Enhanced AI Analysis**
  - Predictive analytics for patient outcomes
  - Sentiment analysis of patient feedback
  - Automated reporting with key insights

- [ ] **Advanced Visualizations**
  - 3D visualization of patient journeys
  - Geographical distribution maps
  - Custom chart builder

- [ ] **Integration Capabilities**
  - Direct EHR system connections
  - Real-time data streaming
  - Multi-source data synchronization

## 👥 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<details>
<summary>Development Guidelines</summary>

- Follow the existing code style
- Write unit tests for new features
- Update documentation as needed
- Follow conventional commit messages
</details>

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

**Made with ❤️ by [SquizAI](https://github.com/SquizAI)**

[Report Bug](https://github.com/SquizAI/EHR_MC_Dashboard/issues) • [Request Feature](https://github.com/SquizAI/EHR_MC_Dashboard/issues)

</div>
