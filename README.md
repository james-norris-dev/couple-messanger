# Couple Messenger

> Secure messaging platform for couples with AI-assisted communication

[![Java](https://img.shields.io/badge/Java-17-orange)](https://openjdk.org/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.2-brightgreen)](https://spring.io/projects/spring-boot)
[![React](https://img.shields.io/badge/React-18-blue)](https://reactjs.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 🎯 Overview

A private messaging application designed for couples to communicate more openly using AI-powered message suggestions. Built with Spring Boot, React, and integrated with LLM APIs for intelligent message generation.

**Status:** 🚧 In Development (MVP Phase)

## ✨ Features (Planned MVP)

- 🔐 **Secure Pairing System** - Verify your partner with unique 6-digit codes
- 💬 **Real-time Messaging** - WebSocket-based instant communication
- 🤖 **AI Message Generation** - Get suggestions when words are hard to find
- 🎨 **Tone Selection** - Choose from playful, romantic, direct, or teasing styles
- 🔒 **End-to-End Encryption** - Your messages stay private
- 📱 **Responsive Design** - Works on desktop and mobile browsers

## 🛠️ Tech Stack

### Backend
- **Java 17** with Spring Boot 3.2
- **Spring Security** + JWT authentication
- **Spring WebSocket** for real-time messaging
- **MySQL 8.0** database
- **OpenAI/Anthropic API** for AI generation

### Frontend
- **React 18** with functional components
- **React Router v6** for navigation
- **STOMP.js** for WebSocket client
- **Tailwind CSS** for styling

## 🚀 Getting Started

### Prerequisites
- Java 17+
- Node.js 18+
- MySQL 8.0
- Maven 3.8+

### Backend Setup
```bash
cd backend
cp src/main/resources/application.properties.example application.properties
# Edit application.properties with your database credentials
mvn clean install
mvn spring-boot:run
```

### Frontend Setup
```bash
cd frontend
npm install
npm start
```

Access the app at `http://localhost:3000`

## 📁 Project Structure
```
couple-messenger/
├── backend/                 # Spring Boot REST API
│   ├── src/main/java/
│   │   └── com/yourname/couples/
│   │       ├── config/     # Security, WebSocket config
│   │       ├── controller/ # REST endpoints
│   │       ├── model/      # JPA entities
│   │       ├── repository/ # Data access
│   │       ├── service/    # Business logic
│   │       └── security/   # JWT implementation
│   └── pom.xml
└── frontend/                # React application
    ├── src/
    │   ├── components/     # React components
    │   ├── services/       # API integration
    │   └── hooks/          # Custom hooks
    └── package.json
```

## 🔑 Environment Variables

Create `.env` files in both backend and frontend:

**Backend (`backend/src/main/resources/application.properties`):**
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/couples_app
spring.datasource.username=your_username
spring.datasource.password=your_password
jwt.secret=your-secret-key
openai.api.key=your-openai-key
```

**Frontend (`frontend/.env`):**
```
REACT_APP_API_URL=http://localhost:8080
REACT_APP_WS_URL=ws://localhost:8080/ws
```

## 📋 Development Roadmap

- [x] Project setup and architecture planning
- [ ] User authentication (JWT)
- [ ] Pairing system implementation
- [ ] Real-time messaging with WebSocket
- [ ] AI integration (message generation)
- [ ] Frontend UI components
- [ ] End-to-end encryption
- [ ] Deployment

## 🤝 Contributing

This is a personal portfolio project, but feedback and suggestions are welcome! Feel free to open an issue.

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details

## 👤 Author

**James [Your Last Name]**
- GitHub: [@yourusername](https://github.com/yourusername)
- LinkedIn: [Your Profile](https://linkedin.com/in/yourprofile)
- Portfolio: [yourwebsite.com](https://yourwebsite.com)

---

**Built as a portfolio project demonstrating full-stack development, real-time communication, and AI integration.**
