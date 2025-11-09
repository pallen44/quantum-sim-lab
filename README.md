# quantum-sim-lab

**Purpose:** A learning-first sandbox to compare **classical** and **quantum-inspired** approaches to small problems (optimization & simple ML), with tests-first development and short ADRs to cement understanding.

**Why this exists:** I want real outcomes *and* real learning. This repo uses an AI-assisted workflow where I (1) write specs/tests, (2) let AI implement to my tests, and (3) document tradeoffs via short ADRs.

---

## 🧭 Roadmap (phased)

- **Phase 1 — Foundations (Weeks 1–2)**
  - Build and test simple circuits: Hadamard, CNOT, Bell state; measure distributions.
  - Deliverables: `src/quantum/basic_gates.py`, `tests/test_basic_gates.py`, `docs/adr/ADR-001.md`.

- **Phase 2 — Optimization (Weeks 3–5)**
  - Classical Simulated Annealing vs **QAOA** on toy graphs (e.g., 4–8 nodes MaxCut).
  - Deliverables: `src/classical/simulated_annealing.py`, `src/quantum/qaoa_solver.py`, tests, ADR-002.

- **Phase 3 — Quantum ML (Weeks 6–8)**
  - Simple hybrid model (quantum layer + classical classifier) on tiny dataset.
  - Deliverables: `src/quantum/qml_model.py`, tests, ADR-003.

---

## 🧰 Tech Stack

- **Python 3.11+**
- **Qiskit** (primary), optional **PennyLane** later
- **NumPy / SciPy / scikit-learn**
- **pytest** for tests

> Initial deps (pin later):  
> `pip install qiskit numpy scipy scikit-learn pytest`

Create a venv:
```bash
python -m venv .venv && source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -U pip
pip install qiskit numpy scipy scikit-learn pytest
