# DoR — Definition of Ready for Requirements Demand

> **Status:** DRAFT  
> **Auftrag:** Daniel → Paul  
> **Quelle:** Confluence "DoR for Requirements Demand" (erstellt: Tamer Abdulghani, zuletzt editiert: Jaco Wessels, 31.03.2026)  
> **Nächster Termin:** Mittwoch-Meeting mit Daniel

---

## 1. Aufgabenstellung

Daniel hat Paul beauftragt, die Confluence-Seite "DoR for Requirements Demand" in ein strukturiertes Dokument zu überführen:

- Confluence-Inhalt in ein Word-/Excel-Dokument überführen
- Alles auf Englisch
- Standardfragen extrahieren (Fragen, die immer kommen)
- Service-Beschreibungen standardisieren
- Fragen standardisieren in Natural Language
- Ziel: Grundlage für "Request Something" Landing Page

---

## 2. Erstellte Dokumente

| # | Dokument | Beschreibung |
|---|----------|--------------|
| 1 | `AI_CoE_DoR_Service_Catalog.xlsx` | Excel-Hauptdokument: 6 Sheets (Sheet 0 + 5 Cluster), 3-stufige Fragen-Hierarchie, Farbcodierung |
| 2 | `AI_CoE_DoR_Service_Catalog_v1.docx` | Word v1 — Slide-konform, 5 Cluster, 12 Seiten |
| 3 | `AI_CoE_DoR_Service_Catalog.docx` | Word v2 — Standard Question Library + Service-Specific Questions, 12 Seiten |

---

## 3. Architektur: 3-stufige Fragen-Hierarchie

```
Sheet 0: Universal Intake          → Gilt fuer JEDEN Request
   └── Cluster-Level               → Gilt fuer alle Services im Cluster
         └── Service-Level          → Nur service-spezifische Zusatzfragen
```

---

## 4. DEMO Questionnaire

> Dieses Questionnaire bildet die vollstaendige 3-Ebenen-Hierarchie ab.  
> Zweck: Diskussionsgrundlage fuer das Mittwoch-Meeting mit Daniel.

---

### Sheet 0 — Universal Intake

*Diese Fragen gelten fuer jeden Request, unabhaengig vom Service.*

| # | Question | Required | Field Type | Notes |
|---|----------|----------|------------|-------|
| 0.1 | Your name | Yes | Auto-filled | Pulled from system |
| 0.2 | Your email | Yes | Auto-filled | Pulled from system |
| 0.3 | Your department | Yes | Auto-filled | Pulled from system |
| 0.4 | What is a short name for your request? | Yes | Text | Brief title for tracking |
| 0.5 | What do you need help with? | Yes | Dropdown → routes to Cluster/Service | Core routing question |
| 0.6 | Who is the business sponsor or owner? | Yes | Text | Name + contact |
| 0.7 | How urgent is this? (Low / Medium / High / Critical) | Yes | Dropdown | SLA-relevant |
| 0.8 | Does your manager support this request? | Yes | Yes/No | Approval gate |
| 0.9 | Do you have a SEGA ID? (if available) | No | Text | Optional — leave blank if none |
| 0.10 | Any documents to share? | No | File Upload | Supporting materials |
| 0.11 | Anything else we should know? | No | Text (multiline) | Free-form context |

---

### Cluster 1 — Discover & Ideate

**Cluster-Level Questions:**

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| C1.1 | What business problem are you trying to solve? | Yes | Text (multiline) |
| C1.2 | Who are the end users or beneficiaries? | Yes | Text |
| C1.3 | What does success look like for you? | Yes | Text (multiline) |

#### 1.1 AI Opportunity Assessment

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 1.1.1 | Which process or workflow should we assess? | Yes | Text |
| 1.1.2 | What data sources are currently involved? | Yes | Text (multiline) |
| 1.1.3 | Are there known pain points or bottlenecks? | No | Text (multiline) |

#### 1.2 Use Case Discovery Workshop

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 1.2.1 | How many participants do you expect? | Yes | Number |
| 1.2.2 | Preferred date(s) and duration? | Yes | Date + Dropdown |
| 1.2.3 | Any specific topics or areas to focus on? | No | Text (multiline) |

#### 1.3 Proof of Concept (PoC)

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 1.3.1 | What is the hypothesis you want to validate? | Yes | Text (multiline) |
| 1.3.2 | What key data sources, APIs, or connectors are needed? | Yes | Text (multiline) |
| 1.3.3 | What is the expected timeline for the PoC? | Yes | Dropdown (2 weeks / 4 weeks / 6 weeks / other) |
| 1.3.4 | What are the success criteria? | Yes | Text (multiline) |

---

### Cluster 2 — Design & Validate

**Cluster-Level Questions:**

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| C2.1 | What systems or data sources are involved? | Yes | Text (multiline) |
| C2.2 | Any existing documentation or diagrams? (not required — architecture diagram asked separately for reviews) | No | File Upload |
| C2.3 | What is the data classification? (Public / Internal / Confidential / Strictly Confidential) | Yes | Dropdown |

#### 2.1 Architecture Consulting

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 2.1.1 | What are you trying to build or design? | Yes | Text (multiline) |
| 2.1.2 | Are there cloud or infrastructure constraints? | No | Text |
| 2.1.3 | What is your current tech stack? | Yes | Text (multiline) |

#### 2.2 Architecture Review

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 2.2.1 | Please upload your architecture diagram | Yes | File Upload |
| 2.2.2 | Has a threat model been completed? | Yes | Yes/No |
| 2.2.3 | What are the key non-functional requirements? (performance, availability, security) | Yes | Text (multiline) |

#### 2.3 Engineering Consulting

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 2.3.1 | What phase is your project in? (Early idea / Mid-development / Already built) | Yes | Dropdown |
| 2.3.2 | Who is the target audience? | Yes | Text |
| 2.3.3 | What is the team's AI/ML knowledge level? (Beginner / Intermediate / Advanced) | Yes | Dropdown |
| 2.3.4 | What specific engineering challenge do you need help with? | Yes | Text (multiline) |

#### 2.4 PoC Validation

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 2.4.1 | Link to the original PoC request or results | Yes | URL / Text |
| 2.4.2 | What key data sources, APIs, or connectors were used? | Yes | Text (multiline) |
| 2.4.3 | What were the PoC results? | Yes | Text (multiline) |
| 2.4.4 | Go / No-Go recommendation? | Yes | Dropdown (Go / No-Go / Needs more data) |

---

### Cluster 3 — Build & Scale

**Cluster-Level Questions:**

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| C3.1 | What phase is your project in? (Early idea / Mid-development / Already built) | Yes | Dropdown |
| C3.2 | Who are the target users? | Yes | Text |
| C3.3 | Who is the target audience? | Yes | Text |
| C3.4 | What is the team's AI/ML knowledge level? (Beginner / Intermediate / Advanced) | Yes | Dropdown |

#### 3.1 Custom Model Development

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 3.1.1 | What task should the model perform? | Yes | Text (multiline) |
| 3.1.2 | What training data is available? | Yes | Text (multiline) |
| 3.1.3 | What are the performance requirements? (latency, accuracy) | Yes | Text |
| 3.1.4 | Where should the model be deployed? | Yes | Text |

#### 3.2 Agentic Application Development

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 3.2.1 | What should the agent do? Describe the workflow. | Yes | Text (multiline) |
| 3.2.2 | What tools or systems should the agent interact with? | Yes | Text (multiline) |
| 3.2.3 | What are the guardrails or constraints? | Yes | Text (multiline) |

#### 3.3 Engineering Enablement

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 3.3.1 | What does your team need to be enabled on? | Yes | Text (multiline) |
| 3.3.2 | How many team members need enablement? | Yes | Number |
| 3.3.3 | Preferred format? (Workshop / Pairing / Documentation / Async) | Yes | Dropdown |

---

### Cluster 4 — Platform & Integration

**Cluster-Level Questions:**

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| C4.1 | What is the data classification? (Public / Internal / Confidential / Strictly Confidential) | Yes | Dropdown |
| C4.2 | What is the expected number of users? | Yes | Number |

#### 4.1a GenAI Hub — Onboarding

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 4.1a.1 | Contact person / email for onboarding coordination? | Yes | Text |
| 4.1a.2 | LIAM group(s) for access? | Yes | Text |
| 4.1a.3 | Which Hub features do you need? | Yes | Checkbox (Chat / Assistants / API Access / Custom Apps) |
| 4.1a.4 | Expected number of users in your team? | Yes | Number |

#### 4.1b GenAI Hub — Custom Application

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 4.1b.1 | What should the custom app do? | Yes | Text (multiline) |
| 4.1b.2 | What data sources should it connect to? | Yes | Text (multiline) |
| 4.1b.3 | Any UI/UX requirements? | No | Text (multiline) |

#### 4.2 AI Platform Services

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 4.2.1 | What platform capability do you need? | Yes | Text (multiline) |
| 4.2.2 | What is your deployment target? (Azure / AWS / On-Prem) | Yes | Dropdown |
| 4.2.3 | Any specific SLA requirements? | No | Text |

#### 4.3a MCP Server — New

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 4.3a.1 | What backend system should the MCP server connect to? | Yes | Text |
| 4.3a.2 | How many consumers are expected? | Yes | Number |
| 4.3a.3 | Do you have a OneTrust ID? | No | Text |
| 4.3a.4 | What operations should the MCP server expose? | Yes | Text (multiline) |

#### 4.3b MCP Server — Connect Existing

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 4.3b.1 | Which existing MCP server do you want to connect to? | Yes | Text |
| 4.3b.2 | How many consumers are expected? | Yes | Number |
| 4.3b.3 | What is your use case for this connection? | Yes | Text (multiline) |

#### 4.4 GitHub Repository Request

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 4.4.1 | Desired repository name? | Yes | Text |
| 4.4.2 | Public or private? | Yes | Dropdown |
| 4.4.3 | LIAM group(s) for access? | Yes | Text |
| 4.4.4 | What will the repo be used for? | Yes | Text (multiline) |

---

### Cluster 5 — Learn & Adopt

**Cluster-Level Questions:**

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| C5.1 | What is the team's current AI knowledge level? (Beginner / Intermediate / Advanced) | Yes | Dropdown |
| C5.2 | How many participants? | Yes | Number |

#### 5.1 AI Training / Workshop

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 5.1.1 | What topic(s) are you interested in? | Yes | Checkbox (Prompt Engineering / LLM Basics / Agentic AI / RAG / Custom Models / Other) |
| 5.1.2 | Preferred format? (In-person / Virtual / Hybrid) | Yes | Dropdown |
| 5.1.3 | Preferred date(s)? | Yes | Date |
| 5.1.4 | Any specific learning objectives? | No | Text (multiline) |

#### 5.2 Change Management Support

| # | Question | Required | Field Type |
|---|----------|----------|------------|
| 5.2.1 | What AI initiative needs change management? | Yes | Text (multiline) |
| 5.2.2 | What stakeholder groups are affected? | Yes | Text (multiline) |
| 5.2.3 | What resistance or concerns have you encountered? | No | Text (multiline) |

---

## 5. Architektur-Entscheidungen

### Was nach oben verschoben wurde (und warum)

| Frage | Von → Nach | Begruendung |
|-------|-----------|-------------|
| SEGA ID | 5 Services ueber 3 Cluster → Sheet 0 | Erschien in 5 Services. Optional — wer keine hat, laesst leer. |
| Business Owner/Sponsor | Cluster 3 + 4.1a → Sheet 0 | Fast jeder Request hat einen Business Owner. |
| Urgency | Nur Cluster 3 → Sheet 0 | Relevant fuer alle Services. |
| Manager Approval | Cluster 3 + Hub Access → Sheet 0 | Gilt ueberall. |
| Supporting Documents | Nur Cluster 3 → Sheet 0 | Nuetzlich fuer jeden Request. |
| Additional Context | Nur Cluster 3 → Sheet 0 | Universell nuetzlich. |
| Phase (Early/Mid/Built) | 2.3 + 3.3 → Cluster 3 | Identische Frage in 2 Services. |
| Target Audience | 2.3 + 3.3 → Cluster 3 | Identische Frage in 2 Services. |
| Knowledge Level | 2.3 + 3.3 → Cluster 3 | Identische Frage in 2 Services. |
| Target Users | 3.2 Agentic App → Cluster 3 | Relevant fuer alle Build-Services. |
| Business Owner | 4.1a Onboarding → Sheet 0 | Universal relevant. |

### Was bewusst NICHT verschoben wurde

| Frage | Bleibt in | Begruendung |
|-------|----------|-------------|
| Data Classification | 6x in einzelnen Services | Entscheidung offen — D1 noch zu klaeren |
| Cloud constraints | 2.1 Arch Consulting | Nur fuer Architecture relevant |
| Threat model | 2.2 Arch Review | Nur fuer Review relevant |
| LIAM groups | 4.1a + 4.4 GitHub | Unterschiedlicher Kontext |
| Consumer count | 4.3a + 4.3b MCP | Nur MCP-Services |

### Duplikat-Eliminierung

| Was | Vorher | Nachher |
|-----|--------|---------|
| C1: PoC "Key Data Sources" | Duplikat mit Cluster 2 "Systems/Data Sources" | Aus PoC entfernt → Cluster-Frage deckt ab. ABER: spezifischere PoC-Frage (APIs, Connectors) fehlt jetzt — muss zurueck. |
| C2: Cluster 2 "Docs/Diagrams" vs. Review "Architecture Diagram" | Verwirrend aehnlich | Cluster-Frage umformuliert: "Any existing docs? (not required — architecture diagram asked separately for reviews)" |

---

## 6. Design-Prinzipien

1. **Standard ≠ Service** — Trennung ist intentional und kritisch fuer skalierbare Intake-Prozesse
2. **Architecture Consulting ≠ Architecture Review** — Zwei getrennte Services (Daniel hatte sie kombiniert auf der Slide, aber im DoR sind es separate Fragenkataloge)
3. **Engineering Enablement** — Eigenstaendiger Service unter Build & Scale (nicht gleich wie Engineering Consulting)
4. **Auto-filled Felder** — Name, Email, Department werden vom System gezogen, nicht vom User eingetippt
5. **Sprach-Vereinheitlichung** — Alle simplified Questions in konsistenter "you/your"-Ansprache, kurze Saetze, Dropdown-Optionen in der Frage sichtbar

---

## 7. Offene Punkte

### Noch zu fixen (3 fehlende Fragen)

| # | Frage | Sheet | Status |
|---|-------|-------|--------|
| 1 | "What phase?" zurueck in 2.3 Engineering Consulting | 2. Design & Validate | Open |
| 2 | "Key Data Sources / APIs / Connectors" zurueck in 2.4 PoC | 2. Design & Validate | Open |
| 3 | "Contact Person / Email for onboarding coordination" zurueck in 4.1a | 4. Platform & Integration | Open |

### Noch zu klaeren (mit Tamer/Daniel)

| # | Thema | Frage |
|---|-------|-------|
| F2 | LIAM Roles Creation | Ist das ein eigenstaendiger Service oder Teil von GitHub Repo Request? In Confluence als separate Zeile erwaehnt. |
| D1 | Data Classification | 6x die gleiche Frage. Zu Universal hochziehen? Oder bewusst pro Service belassen? |
| D2 | SEGA vs. OneTrust ID | In Universal steht "SEGA ID", in MCP steht "OneTrust ID". Zusammenfuehren zu "SEGA or OneTrust ID"? |

---

## 8. Confluence-Quelle

| Feld | Wert |
|------|------|
| Seite | "DoR for Requirements Demand" unter Use Case Mgmt |
| Erstellt von | Tamer Abdulghani |
| Zuletzt editiert von | Jaco Wessels (31.03.2026) |
| Status | DRAFT PAGE |
| Lead Architecture | Tamer |
| Lead GenAI Hub | Tamer |
| Lead MCP | Tamer / DTT |
| Lead GitHub | Tamer / DTT |
| Lead Engineering | Andriy |
| Lead AI Platform | Jaco |
| Lead Training | AI Change Manager |

---

## 9. Naechste Schritte

1. ~~Excel erstellen~~ Done
2. ~~Word v1 + v2 erstellen~~ Done
3. ~~DEMO Questionnaire als Markdown~~ Done
4. 3 fehlende Fragen fixen (Phase in 2.3, Data Sources in 2.4, Contact in 4.1a)
5. Mittwoch-Meeting mit Daniel: Questionnaire praesentieren, Feedback einholen
6. Offene Punkte F2, D1, D2 mit Tamer klaeren
7. Nach Feedback: finale Version fuer Confluence, Jira, Hub, Landing Page adaptieren
