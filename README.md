# 🏦 KOSCOM AI Agent Platform

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![FastAPI](https://img.shields.io/badge/FastAPI-Framework-009688?logo=fastapi)
![Docker](https://img.shields.io/badge/Docker-Containerized-2496ED?logo=docker)
![MCP](https://img.shields.io/badge/Architecture-MCP%20Multi--Agent-orange)
![Status](https://img.shields.io/badge/Project-Academic%20Research-success)
![Domain](https://img.shields.io/badge/Domain-Financial%20AI-critical)

MCP (Model Context Protocol) 기반 금융 데이터 분석 및 감사 자동화를 위한  
멀티 에이전트 AI 플랫폼입니다.

본 프로젝트는 은행 리스크 모니터링, 준비금 검증, 감사 추적(Audit), 보고서 생성 기능을  
각각 독립적인 MCP 서버로 구성하여 확장 가능한 금융 AI Agent 구조를 구현합니다.

---

# 📌 Overview

본 시스템은 금융기관의 건전성 검증과 데이터 신뢰성 확보를 목표로 설계된  
멀티 MCP Agent 아키텍처입니다.

각 기능은 독립적인 MCP 서버로 동작하며 Gateway를 통해 통합됩니다.

### 지원 기능

- Bank Risk Monitoring
- Disclosure & Policy Checking
- KRW Reserve Verification
- Audit Trail Verification
- Financial Report Generation
- Web Dashboard Visualization

---

# 🧠 Architecture

```
User
  ↓
Web Dashboard
  ↓
MCP Gateway
  ↓
MCP Servers

├── Bank Monitoring Agent
├── Audit Verification Agent
├── KRW Reserve Validation Agent
└── Report Generator Agent
```

각 MCP 서버는 독립 실행 가능하며 Tool 단위 확장이 가능합니다.

---

# 📂 Project Structure

```
final_koscom_ai_agent
├── backend
├── frontend
├── infra
│   └── docker
├── mcp_servers
│   ├── bank_monitoring
│   ├── koscom_audit
│   └── krw-full-reserve
```

각 MCP 서버 내부 구조:

```
app_mcp/
core/
tools/
config/
data/
```

---

# ⚙️ MCP Servers

## 1️⃣ Bank Monitoring Server

은행 리스크 분석 및 정책 위반 여부 탐지

기능:

- 은행 신용 리스크 분석
- 정책 위반 탐지
- 공시 데이터 기반 검증
- DART 재무 데이터 분석

---

## 2️⃣ Audit Verification Server

금융 데이터 무결성 검증 및 감사 추적 시스템

기능:

- Merkle 기반 데이터 무결성 검증
- Proof Pack 생성
- InfluxDB 기반 로그 추적
- 블록체인 데이터 검증 (Etherscan)

---

## 3️⃣ KRW Full Reserve Server

KRW 준비금 100% 보유 여부 검증

기능:

- 온체인 준비금 검증
- 오프체인 데이터 비교
- 준비금 커버리지 계산
- 시나리오 기반 검증 리포트 생성

---

# 🖥 Frontend Dashboard

웹 기반 대시보드 제공

지원 기능:

- 채팅 기반 Agent 인터페이스
- 금융 데이터 시각화
- Reserve 상태 확인
- Audit 결과 조회

경로:

```
frontend/templates/
```

---

# 🐳 Infrastructure

Docker 기반 실행 환경 제공

경로:

```
infra/docker
```

포함 구성:

- API container
- Worker container
- InfluxDB container

실행 방법:

```bash
docker compose up --build
```

---

# 🔄 Example MCP Tool Flow

```
Check bank risk status
→ Retrieve financial disclosure
→ Evaluate policy compliance
→ Generate structured report
```

---

# 🔐 Security Notice

보안상의 이유로 다음 항목은 repository에 포함되지 않습니다:

- API keys
- Database credentials
- Slack webhook
- SMTP credentials

`.env.example` 파일을 참고하여 환경 변수를 설정하세요.

---

# 🚀 How to Run

### 1️⃣ Clone repository

```bash
git clone https://github.com/your-repo-url.git
```

### 2️⃣ Setup environment

```bash
cp .env.example .env
```

### 3️⃣ Run docker services

```bash
docker compose up --build
```

---

# 🧩 Extending the Agent

새로운 MCP 서버 추가 방법:

1. 새로운 server 디렉토리 생성
2. tool 정의
3. gateway 연결
4. config 등록

예시:

```
mcp_servers/new_agent
```

---

# 🛠 Tech Stack

### Backend

- Python
- FastAPI
- MCP Protocol

### Database

- PostgreSQL
- InfluxDB

### Infrastructure

- Docker
- Docker Compose

### Frontend

- HTML Dashboard
- Web Chat Interface

---

# 📊 Use Cases

본 플랫폼은 다음 환경에서 활용 가능합니다:

- 금융기관 내부 감사 자동화
- 준비금 검증 시스템
- 정책 위반 탐지
- 리스크 모니터링 자동화
- 규제 대응 보고서 생성

---

# 👤 Author

Industrial Engineering + AI Agent System Design

Focused on MCP-based Financial AI Infrastructure
