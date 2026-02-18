# TrialVault: Clinical Trial Dashboard

TrialVault is a next-generation tool for clinical trial management. For the first time, users within the clinical research community will have real-time active transparency into medical research. With TrialVault, clinical research will become simpler and more straightforward as TrialVault will actively improve participant recruitment and will reduce the administrative burden associated with clinical research for sponsors and investigators. Above all, TrialVault will enhance the clinical research process as a whole.

## 🛠 Technology Stack

### Backend (Java/Spring Boot)
*   **Java 23**: The core language for business logic.
*   **Spring Boot 3.4.2**: Use for the REST API and dependency injection.
    *   **Spring Data JPA**: Abstraction for database interactions.
    *   **H2 Database**: In-memory SQL database for rapid development and testing.
*   **Maven**: Dependency management and build automation.

### Frontend (React/TypeScript)
*   **React 19**: Component-based UI library.
*   **TypeScript**: Ensures type safety and clearer code structure.
*   **Vite**: Next-generation frontend tooling for fast builds.
*   **Tailwind CSS v4**: Utility-first CSS framework for responsive, modern design.
*   **Lucide React**: Beautiful, consistent icons.
*   **Axios**: Promise-based HTTP client for API communication.

## 🏗 Architecture

1.  **Presentation Layer (Frontend)**: React components (`Header`, `StatsCard`, `TrialTable`) consume the API to render dynamic content.
2.  **API Layer (Backend Controller)**: `TrialController.java` exposes REST endpoints (e.g., `GET /api/trials`).
3.  **Service Layer (Business Logic)**: `TrialService.java` encapsulates business rules, decoupling the controller from data access.
4.  **Data Access Layer (Repository)**: `TrialRepository.java` extends `JpaRepository` for standard CRUD operations.
5.  **Database**: H2 in-memory database stores trial data during runtime.

## 🏁 Getting Started

Follow these instructions to set up the project locally.

### Prerequisites
*   Java 23 (or compatible JDK)
*   Node.js & npm
*   Maven

### 1. Run the Backend
Navigate to the backend directory and start the Spring Boot server:

```bash
cd clinical-trial-dashboard/backend
mvn clean spring-boot:run
```

The backend API will start at `http://localhost:8080/api/trials`.

### 2. Run the Frontend
Open a new terminal, navigate to the frontend directory, install dependencies (first time only), and start the dev server:

```bash
cd clinical-trial-dashboard/frontend
npm install
npm run dev
```

The application will be accessible at `http://localhost:5173`.

## 📂 Project Structure

```
clinical-trial-dashboard/
├── backend/                 # Spring Boot Application
│   ├── src/main/java/       # Source code (Controllers, Services, Models)
│   ├── src/main/resources/  # Config (application.properties) & Data (data.sql)
│   └── pom.xml              # Maven dependencies
└── frontend/                # React Application
    ├── src/                 # Source code (Components, Pages, API)
    ├── vite.config.ts       # Vite configuration
    └── package.json         # NPM dependencies
```

## © Copyright
© 2026 Jaisuraj Kaleeswaran. All rights reserved.
