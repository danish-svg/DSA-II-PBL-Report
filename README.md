# Intelligent Election Management System (IEMS)

An intelligent, secure, and transparent web-based election management platform designed to streamline voter authentication, vote casting, and real-time result auditing. The system mitigates traditional electoral challenges such as identity fraud, manual counting discrepancies, and lack of transparency.

---

## Key Features

* **Secure Voter Authentication:** Role-based access control with multi-factor verification to ensure eligible, authenticated voting and prevent duplicate ballots.
* **Voter Anonymity & Data Integrity:** Decoupled voter records and ballot storage to guarantee privacy while preserving verifiable audit logs.
* **Real-Time Analytics Dashboard:** Dynamic visualization of voter turnout, demographics, and live tallying for authorized election administrators.
* **Admin Management Console:** End-to-end management of candidates, constituency boundaries, voting windows, and electoral audit reports.
* **Responsive & Accessible UI:** Modern interface optimized for desktop, tablet, and mobile devices.

---

## Tech Stack

### Frontend
* **Framework:** React with TypeScript
* **Styling:** Tailwind CSS
* **Icons & UI Utilities:** Lucide React / Headless UI
* **State Management & Data Fetching:** Axios, React Query

### Backend
* **Framework:** FastAPI (Python 3.11+)
* **ORM:** SQLAlchemy / SQLModel
* **Data Validation:** Pydantic
* **Security:** Passlib (Bcrypt), Python-Jose (JWT Tokens)

### Database
* **Relational Database:** PostgreSQL

---

## System Architecture

```text
  [ Voter / Admin ]
          │
          ▼
   React Frontend (TypeScript + Tailwind CSS)
          │
      REST APIs (JSON / JWT)
          │
          ▼
   FastAPI Application Gateway
     ├── Auth & Verification Service
     ├── Ballot Encryption & Ingestion Engine
     └── Analytics & Audit Aggregator
          │
          ▼
   PostgreSQL Database (Partitioned Tables & Strict ACID Constraints)
