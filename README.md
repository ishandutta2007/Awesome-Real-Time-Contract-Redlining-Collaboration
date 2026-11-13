# Awesome-Real-Time-Contract-Redlining-Collaboration

# Awesome Real-Time Contract Redlining & Collaboration

> A curated list of top Real-Time Contract Redlining and Collaboration platforms — both SaaS/Hosted commercial CLM and negotiation suites and open-source alternatives for co-editing, tracking changes, and negotiating contracts in real time.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Icertis Vera Engage](#icertis-vera-engage)
  - [Ironclad Editor](#ironclad-editor)
  - [SpotDraft](#spotdraft)
  - [Concord](#concord)
  - [Microsoft Word Online](#microsoft-word-online)
  - [Google Docs](#google-docs)
- [Open-Source Software](#-open-source-software)
  - [draftLegal](#draftlegal)
  - [AI WorkDeck](#ai-workdeck)
  - [Nextcloud Write](#nextcloud-write)
  - [Euro-Office](#euro-office)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Real-Time Contract Redlining and Collaboration platforms. These are not open-source but are included as reference points for feature comparison.

### Icertis Vera Engage
**Type:** Agent-driven drafting and redlining inside enterprise CLM  
Icertis Vera Engage introduces an AI-first experience layer that transforms how users work with contracts, letting teams draft, review, and understand agreements through conversational interactions [citation:3]. The **Redline Agent** applies enterprise rules instantly, flags unacceptable clauses, suggests aligned alternatives, and accelerates reviews, enabling business teams to deliver consistent work without repeated legal intervention [citation:3]. **AI-Generated Playbooks** convert real contracts, past negotiations, and expert guidance into structured playbooks within minutes, giving enterprises clear rules and fallbacks even when no formal standards existed before [citation:3]. The **Risk Review Agent** explains clauses, compares drafts, and surfaces insights in plain language [citation:3].  
**Best for:** Enterprises already using Icertis CLM wanting agent-driven redlining and playbook creation without leaving their contract intelligence platform.

### Ironclad Editor
**Type:** In-platform document editing with tracked changes and redline import  
Ironclad Editor provides a central place for document revisions, allowing legal teams to edit, redline, and version DOC, DOCX, and PDF attachments directly in Ironclad [citation:4]. **Track Changes** can be toggled on to label all edits as redlines, with the ability to accept or reject individual changes in the sidebar [citation:4]. **Edit from Redlines** allows comparing versions and editing differences directly [citation:4]. **Incorporate Counterparty Changes** imports redlined contracts sent via email, including comments and tracked changes, for review within the platform [citation:4]. The **Contract Review Agent** (formerly Jurist) allows highlighting a specific clause and instructing the AI to make precise changes, displayed as highlighted redlines for easy review [citation:11]. **Limitations:** Certain track changes are unsupported or unrendered, including table row insertions/deletions and content control fields [citation:4].  
**Best for:** Enterprise legal teams already on Ironclad wanting in-platform redlining with counterparty change import and AI-assisted clause editing.

### SpotDraft
**Type:** AI-assisted negotiation with native Microsoft Word integration  
SpotDraft's **VerifAI** applies playbook-based review to counterparty paper, flagging clause-level risk and suggesting redlining in Microsoft Word, with findings connected straight into SpotDraft's approval workflow [citation:1]. The **MS Word Desktop integration** allows opening contracts directly in Word from SpotDraft, making edits, and saving back automatically without download/re-upload friction [citation:5]. The integration provides visibility into who else is reviewing, distinguishes internal vs. external comments, and organizes version saves as drafts and published versions [citation:5]. SpotDraft's data showed that **99.9% of contract edits are made by a single editor**, and **88% of contracts only have one editor** throughout their lifecycle, which informed the Word-first approach [citation:5]. **Limitation:** VerifAI's output quality depends heavily on playbook configuration; teams with little existing playbook documentation need real setup time [citation:1].  
**Best for:** Legal teams prioritizing formatting fidelity and native Word workflows, particularly those where single-editor redlining is the norm.

### Concord
**Type:** Real-time collaborative redlining with internal-only revisions  
Concord enables real-time redlining on live online contract documents, with each party's revisions color-coded differently [citation:13]. **Revisions** can be toggled to track changes, and other parties see changes instantly via the same shared link [citation:13]. A key differentiator is **internal-only versions**: teams can make changes and comments that are not pushed to the external party until "publish" is clicked [citation:6]. The platform includes an **audit trail** showing who made which changes and when, version history with restore capability, and a discussion panel with public vs. internal comments [citation:6]. Concord supports exporting to Word or Google Docs for external markup, then dragging the updated file back in [citation:6]. A comparison notes Concord leads on **mobile access/redlining** and **real-time collaborative editing** [citation:15].  
**Best for:** Teams wanting real-time collaborative redlining with strong internal/external separation and mobile access, without forcing counterparties onto a specific platform.

### Microsoft Word Online
**Type:** Browser-based Word with co-authoring and track changes  
Word Online provides the familiar Microsoft Word experience in the browser, with real-time co-authoring, comments, and track changes. It is the natural choice for organizations standardized on Microsoft 365, with seamless transition to desktop Word for advanced formatting. For contract redlining specifically, Word's track changes and comments remain the industry-standard lingua franca for legal markup.

### Google Docs
**Type:** Real-time collaborative document editing with suggestion mode  
Google Docs offers real-time co-editing with live cursors, comments, and **Suggestion Mode** which functions as tracked changes for collaborative review. It is widely used for contract collaboration when counterparties are already in the Google ecosystem, though it lacks contract-specific features like playbook enforcement or obligation tracking.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Real-Time Contract Redlining and Collaboration tools. The open-source ecosystem is **nascent and limited** — available projects range from AI-native CLM platforms to general document editors that can be used for contract markup.

### draftLegal
**Stack:** TypeScript / Python / Docker | **License:** AGPL-3.0  
draftLegal is explicitly positioned as **"the open-source alternative to Ironclad + Harvey"** — a self-hosted, AI-native contract lifecycle management platform where contracts never leave your servers [citation:2]. For redlining and negotiation specifically, it provides **conservative / moderate / aggressive counter-proposal options with exact replacement language**, applied in a click [citation:2]. An **agent-first workflow** with ~30 tools over contracts includes redline and route approvals, with every write proposed on a confirm card first and most actions undoable [citation:2]. **Extract + cite** capabilities extract clauses, dates, and values with citations back to the clause and section, and for PDFs the citation opens the original page [citation:2]. **Portfolio intelligence** uses hybrid retrieval (pgvector + Elasticsearch + RRF fusion) to answer questions across the entire contract portfolio [citation:2]. Supports Anthropic, OpenAI, or Google Gemini with bring-your-own-key [citation:2]. **Important:** The project is early-stage; review repository status before production use.  
**Best for:** Teams wanting a self-hosted, AI-native CLM with redlining and counter-proposal generation, accepting early-stage maturity in exchange for full data control.

### AI WorkDeck
**Stack:** Java / TypeScript / Office Add-in | **License:** Open Source (with CLA)  
AI WorkDeck is an open-source workspace for professional document AI, with a focus on legal work including **contract review and source checking** [citation:9]. Its key differentiator for collaboration is **three-way document merge workflows** and **paragraph-level provenance** backed by Git history, allowing parallel drafts to be compared and merged [citation:9]. It provides **source-linked work**: connect a passage to its supporting material, navigate back to the source, and detect changed or missing anchors [citation:9]. The **Office/WPS task panes** connect AI assistance to existing document workflows, and the platform is extensible via plugins and Skills [citation:9]. **Note:** Code contributions require a one-time CLA, with contributors granting dual-licensing rights [citation:9].  
**Best for:** Legal technologists and developers wanting a Git-backed, source-linked document collaboration foundation with three-way merge, accepting the Java/plugin architecture and CLA requirement.

### Nextcloud Write
**Stack:** PHP / Collabora or Euro-Office | **License:** AGPL-3.0  
Nextcloud Write is a full-featured, real-time collaborative document editor that runs entirely on infrastructure of your choice, positioned as a sovereign open-source alternative to Word and Google Docs [citation:7]. For contract collaboration, it provides **real-time co-editing with color-coded cursors** and a **formal review mode** that tracks edits and allows accepting or rejecting changes from collaborators the same way as Word and Google Docs [citation:7]. Documents can be shared via **public links with granular permissions** (read-only, editable, or watermarked), and collaborators can leave comments in the margin attached to the exact passage [citation:7]. **Federated collaboration** allows teams on separate Nextcloud instances to co-author the same document across servers [citation:7]. Changes are saved continuously with **automatic version history**, and **compare and combine** tools reconcile divergent versions [citation:7]. Supports DOCX and ODT formats, with optional AI assistant via Nextcloud Assistant [citation:7].  
**Best for:** Organizations already running Nextcloud or prioritizing data sovereignty wanting real-time collaborative document editing with review mode and version history for contract workflows.

### Euro-Office
**Stack:** JavaScript / AGPL (based on ONLYOFFICE Open Source) | **License:** AGPL-3.0  
Euro-Office provides a truly open, transparent, and sovereign solution for collaborative document editing, designed to be integrated into other products like file sharing solutions, wikis, or project management tools [citation:14]. It supports **real-time collaborative editing of DOCX, PPTX, XLSX, PDF, ODT, ODS, ODP, and TXT** formats [citation:14]. Euro-Office is a fork of the ONLYOFFICE Open Source codebase, extensively reviewed and cleaned up to make it easy to build and contribute to, with the stated goal of removing proprietary sections and binary blobs [citation:14]. It is backed by IONOS, Nextcloud, Proton, XWiki, OpenProject, and others [citation:14]. **Trade-off:** It is an **integration component** rather than a standalone application — storage, navigation, permissions, and sharing logic must be provided by the host application [citation:14].  
**Best for:** Developers building contract collaboration features into their own platforms who want a sovereign, AGPL-licensed document editing engine with real-time collaboration, accepting the integration-component architecture.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Real-Time Co-Editing | Track Changes | AI Redlining | Self-Hosted | Best For |
|----------|---------|-------|----------------------|--------------|--------------|-------------|----------|
| **Icertis Vera** | Proprietary | Cloud | (Conversational) | ✅ | ✅ Redline Agent | ❌ | Agent-driven CLM redlining |
| **Ironclad Editor** | Proprietary | Cloud | (Editor) | ✅ + Import | ✅ Review Agent | ❌ | In-platform + counterparty import |
| **SpotDraft** | Proprietary | Cloud + Word | (Word native) | ✅ | ✅ VerifAI | ❌ | Word-first playbook redlining |
| **Concord** | Proprietary | Cloud | ✅ Color-coded | ✅ | ❌ | ❌ | Real-time + internal-only revisions |
| **draftLegal** | AGPL-3.0 | TypeScript/Docker | (Agent-driven) | ✅ | ✅ Counter-proposals | ✅ | Self-hosted AI CLM + redline |
| **AI WorkDeck** | Open Source | Java/TS | (Three-way merge) | ✅ Git-backed | ✅ Source-linked | ✅ | Git-backed provenance + merge |
| **Nextcloud Write** | AGPL-3.0 | PHP/Collabora | ✅ Color-coded cursors | ✅ Review mode | (Optional AI) | ✅ | Sovereign real-time document editing |
| **Euro-Office** | AGPL-3.0 | JavaScript | ✅ | ✅ | ❌ | ✅ (Component) | Embeddable sovereign editing |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Real-Time Contract Redlining or Collaboration tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source. Note that the open-source ecosystem for **dedicated contract redlining** is **very limited and fragmented**. **draftLegal** is the most direct open-source effort, explicitly targeting the Ironclad + Harvey combination with AI-driven counter-proposals and full lifecycle management [citation:2]. **AI WorkDeck** offers a unique Git-backed provenance and three-way merge approach for document collaboration [citation:9]. For general real-time document collaboration that can be applied to contracts, **Nextcloud Write** provides the strongest sovereign option with color-coded co-editing and review mode [citation:7], while **Euro-Office** offers an embeddable AGPL-licensed editing engine [citation:14]. Commercial platforms like SpotDraft and Ironclad remain far more capable for playbook-enforced redlining and counterparty change management.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
