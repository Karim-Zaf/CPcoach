# Codeforces Coach

**Agent IA multi-agents pour le coaching personnalise en programmation competitive.**

Analyse ton profil Codeforces, identifie tes faiblesses, et te recommande des problemes cibles pour progresser. Hints progressifs temporises, plan d'entrainement personnalise, notifications quotidiennes.

## Statut

> **v0.1 - Proof of Concept** (en cours)
>
> Script Python standalone — analyse de profil + recommandations via l'API Codeforces.

## Fonctionnalites prevues

| Module | Description | Statut |
|---|---|---|
| Profile Analyzer | Analyse tes submissions, detecte tes forces/faiblesses par tag | En cours |
| Problem Recommender | Suggere des problemes dans ta zone optimale (+100 a +200 rating) | En cours |
| Hint Engine | Hints progressifs temporises (1-5 hints, intervalle configurable) | Prevu v0.5 |
| Coach Agent | Agent LangGraph multi-outils avec memoire conversationnelle | Prevu v1.0 |
| RAG Editorials | Recherche semantique sur les editoriaux et blogs CF | Prevu v1.0 |
| Notifications | Emails quotidiens/hebdomadaires avec recommandations | Prevu v1.5 |
| Dashboard | Frontend Next.js avec graphiques de progression | Prevu v1.0 |

## Quick Start

```bash
# Cloner le repo
git clone https://github.com/Karim-Zaf/codeforces-coach.git
cd codeforces-coach

# Setup Python
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Lancer l'analyse de profil
python main.py Kairm_Zaf
```

## Structure du projet

```
codeforces-coach/
├── main.py              # Point d'entree CLI
├── cf_api.py            # Wrapper API Codeforces
├── analyzer.py          # Analyse du profil (forces/faiblesses)
├── recommender.py       # Suggestion de problemes cibles
├── requirements.txt     # Dependances Python
└── README.md
```

## Stack technique

| Couche | Technologie | Phase |
|---|---|---|
| Backend API | FastAPI (Python 3.12) | v0.5 |
| Agents IA | LangGraph + LangChain | v1.0 |
| RAG | ChromaDB → Pinecone | v1.0 |
| LLM | Groq (dev) / Claude API (prod) | v1.0 |
| Frontend | Next.js 14 + TypeScript + Tailwind | v1.0 |
| DB | PostgreSQL + Redis | v0.5 |
| Emails | Resend | v1.5 |
| Deploy | Vercel (front) + Render (back) | v1.0 |

## API Codeforces utilisee

- `user.status` — Submissions d'un utilisateur
- `user.info` — Profil (rating, rank)
- `user.rating` — Historique de rating
- `problemset.problems` — Catalogue complet des problemes

> L'API Codeforces est publique et ne necessite aucune cle.

## Roadmap

- [x] Business plan & specification technique
- [ ] **v0.1** — PoC : analyse de profil + recommandations (CLI)
- [ ] **v0.5** — FastAPI backend + endpoints REST
- [ ] **v1.0** — Agent LangGraph + RAG + frontend Next.js
- [ ] **v1.5** — Notifications + Stripe + auth
- [ ] **v2.0** — Multi-plateforme (LeetCode, AtCoder)

## Auteur

**Karim Zaafrani** ([@Kairm_Zaf](https://codeforces.com/profile/Kairm_Zaf)) — Expert 1870, TCPC Champion

---

*Projet en cours de developpement — Mars 2026*