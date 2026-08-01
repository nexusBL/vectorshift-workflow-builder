# VectorShift Workflow Builder

A workflow builder built as part of the VectorShift Frontend Technical Assessment.

## Features

- Reusable BaseNode component
- Drag-and-drop workflow builder using React Flow
- Dynamic Text Node with variable parsing
- Auto-resizing Text Node
- Dynamic input handles generated from `{{variable}}`
- Backend workflow parsing with FastAPI
- DAG (Directed Acyclic Graph) detection using Kahn's Algorithm
- Pipeline analysis (Nodes, Edges, DAG)

---

## Tech Stack

### Frontend

- React
- React Flow
- Zustand
- Axios

### Backend

- FastAPI
- Python

---

## Project Structure

```
vectorshift-workflow-builder/
│
├── backend/
│   └── main.py
│
├── frontend/
│   ├── src/
│   └── public/
│
├── photo/
│   ├── 1.png
│   └── 2.png
│
└── README.md
```

---

## Installation

### Backend

```bash
cd backend
pip install fastapi uvicorn python-multipart
uvicorn main:app --reload
```

Runs on

```
http://127.0.0.1:8000
```

---

### Frontend

```bash
cd frontend
npm install
npm start
```

Runs on

```
http://localhost:3000
```

---

## Screenshots

### Workflow Builder

![Workflow Builder](photo/1.png)

---

### Pipeline Analysis

![Pipeline Analysis](photo/2.png)

---

## Dynamic Text Node

Supports variables using

```
{{variable}}
```

Example

```
Hello {{name}}

Welcome {{company}}

Email {{email}}
```

Each variable automatically generates an input handle.

---

## Backend Analysis

The backend computes

- Number of Nodes
- Number of Edges
- DAG Detection

using Kahn's Algorithm.

Example response

```json
{
    "num_nodes": 3,
    "num_edges": 2,
    "is_dag": true
}
```

---

## Author

Bharath L