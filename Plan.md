# Plan for Day 11: Guardrails, HITL & Responsible AI

## 🎯 Overview
This lab focuses on securing AI applications by implementing mandatory guardrails, Human-In-The-Loop (HITL) workflows, and performing red teaming to identify vulnerabilities.

## 🏗️ Project Organization
The implementation is distributed across several modules in the `src/` directory:
- `src/attacks/`: Adversarial testing and red teaming.
- `src/guardrails/`: Input/Output validation logic and NeMo Guardrails integration.
- `src/testing/`: Evaluation pipelines to compare "Unsafe" vs "Protected" agents.
- `src/hitl/`: Human-In-The-Loop routing and decision logic.
- `src/agents/`: Agent definitions.

## 📋 The 13 TODOs

| # | Task | Category | Location |
|---|------|----------|----------|
| 1 | Write 5 adversarial prompts | Attacks | `src/attacks/attacks.py` |
| 2 | Generate attack test cases with AI | Attacks | `src/attacks/attacks.py` |
| 3 | Injection detection (regex) | Input Guardrails | `src/guardrails/input_guardrails.py` |
| 4 | Topic filter | Input Guardrails | `src/guardrails/input_guardrails.py` |
| 5 | Input Guardrail Plugin | Input Guardrails | `src/guardrails/input_guardrails.py` |
| 6 | Content filter (PII, secrets) | Output Guardrails | `src/guardrails/output_guardrails.py` |
| 7 | LLM-as-Judge safety check | Output Guardrails | `src/guardrails/output_guardrails.py` |
| 8 | Output Guardrail Plugin | Output Guardrails | `src/guardrails/output_guardrails.py` |
| 9 | NeMo Guardrails Colang config | Guardrails | `src/guardrails/nemo_guardrails.py` |
| 10| Rerun 5 attacks with guardrails | Testing | `src/testing/testing.py` |
| 11| Automated security testing pipeline | Testing | `src/testing/testing.py` |
| 12| Confidence Router (HITL) | HITL | `src/hitl/hitl.py` |
| 13| Design 3 HITL decision points | HITL | `src/hitl/hitl.py` |

## ✅ Implementation Checklist

### 🛡️ Part 1: Attacks & Red Teaming
- [x] **TODO 1**: Write 5 diverse adversarial prompts (Jailbreak, Prompt Injection, PII leakage).
- [x] **TODO 2**: Use AI to generate 10+ adversarial test cases (Red Teaming).
- [x] **Baseline**: Run attacks against the **Unsafe Agent** and record failures.

### 🚧 Part 2: Guardrails Implementation
#### Phase 2A: Input Guardrails
- [ ] **TODO 3**: Implement Regex-based detection for common injection patterns.
- [ ] **TODO 4**: Implement a Topic Filter to restrict off-topic queries.
- [ ] **TODO 5**: Wrap logic into a Google ADK Input Guardrail Plugin.

#### Phase 2B: Output Guardrails
- [ ] **TODO 6**: Implement PII (Email, Phone) and Secret (API Key) detection filters.
- [ ] **TODO 7**: Implement LLM-as-Judge to evaluate response safety/relevance.
- [ ] **TODO 8**: Wrap logic into a Google ADK Output Guardrail Plugin.

#### Phase 2C: NeMo Guardrails
- [ ] **TODO 9**: Configure Colang files for declarative safety boundaries (NVIDIA NeMo).

### 🧪 Part 3: Testing & Pipeline
- [ ] **TODO 10**: Rerun the 5 baseline attacks against the **Protected Agent**.
- [ ] **TODO 11**: Build an automated security testing pipeline to calculate safety scores.
- [ ] **Security Report**: Complete the before/after comparison report.

### 👤 Part 4: Human-In-The-Loop (HITL)
- [ ] **TODO 12**: Implement a Confidence Router to detect uncertain LLM outputs.
- [ ] **TODO 13**: Design 3 specific HITL decision points with escalation paths.
- [ ] **Flowchart**: Create/Update the HITL workflow diagram.

## 🏁 Deliverables
1. **Security Report**: Comparing results before and after guardrails.
2. **HITL Flowchart**: Visualizing the escalation paths.
