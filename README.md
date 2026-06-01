# 🤖 LinkedIn Agents OS

LinkedIn Agents OS is an automated content creation system built with **CrewAI**. It is designed to transform technical developer notes into high-impact, human-like LinkedIn posts, specifically optimized for B2B tech audiences, founders, and engineers.

## 🎯 Overview
The system leverages a multi-agent architecture to ensure content quality:
1. **Copywriter Agent**: Converts complex technical concepts into engaging, scannable LinkedIn posts.
2. **Quality Critic Agent**: Audits the content against LinkedIn's algorithm to maximize *Dwell Time* and remove "AI-sounding" clichés.

## 🏗 Project Structure

```text
linkedin_agents_os/
├── knowledge/          # User preferences & style guides
├── src/
│   ├── linkedin_agents_os/
│   │   ├── config/     # Agent and Task definitions (YAML)
│   │   ├── crew.py     # Crew orchestration logic
│   │   └── main.py     # Entry point and CLI commands
└── pyproject.toml      # Project metadata & dependencies

## ⚙️ Configuration & Personalization
The core of the system is the knowledge/user_preference.txt file. This acts as the "Brain" of the agents, containing:

Project Context: Details about your current focus (e.g., pri0).

Tone & Style: Direct, technical, and human-centric guidelines.

Negative Constraints: A strictly forbidden list of corporate buzzwords to avoid.

## 🚀 Installation
Clone the repository:

Bash
git clone [https://github.com/tu-usuario/linkedin_agents_os.git](https://github.com/tu-usuario/linkedin_agents_os.git)
cd linkedin_agents_os
Install dependencies:

Bash
pip install -r requirements.txt
Set up Environment Variables:
Create a .env file in the root directory:

Fragmento de código
OPENAI_API_KEY=sk-...
SERPER_API_KEY=...
MODEL=gpt-4o

##🛠 Usage
The project provides a CLI interface through linkedin_agents_os:

Run the crew:
linkedin_agents_os run

Train the agents:
linkedin_agents_os train <n_iterations> <filename>

Test performance:
linkedin_agents_os test <n_iterations> <eval_llm>

Custom Trigger:
linkedin_agents_os run_with_trigger "<JSON_PAYLOAD>"

## 💡 Why this project?
This tool solves the "Content vs. Coding" dilemma. Instead of spending hours writing, you feed your daily dev logs (Conda issues, architecture decisions, AI implementation details) and get a professional, algorithm-ready post in seconds. It ensures consistency and maintains a "Build in Public" presence without the burnout.

## 📜 License
MIT © [Miguel Ángel Giraldo Polanco]
