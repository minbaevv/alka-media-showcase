# AlKa Media — Bilingual News Portal

A Russian/Kyrgyz news portal with a Python backend developed by
**Kubanychbek Duishekeev**.

I developed the backend. The React/Vite frontend was built
with AI assistance.

> **Source code is private.**
> This repository contains portfolio documentation only.

## Project Overview

AlKa Media supports publishing news in Russian and Kyrgyz,
organizing articles, searching content and moderating comments.

## 📄 Project Presentation

[View the AlKa Media presentation (PDF)](./AlKa_Media_Case_Study.pdf)

---

**Development period:** 14 August–2 September 2026.

🌐 **Website:** [alkamedia.kg](https://alkamedia.kg)

Current website availability was not verified during the
portfolio documentation review. The archived code may differ
from the current deployment.

## My Contribution

### Backend Development

I developed the Python/FastAPI backend, including:

- Data storage and API functionality
- Article management
- Bilingual content fields
- Search, filtering and pagination
- Administrative authentication
- Image-upload functionality
- Comment submission and moderation

### AI-Assisted Frontend

The React/Vite frontend was built with AI assistance.

I distinguish this contribution from the backend implementation
rather than presenting all frontend code as independently written.

## Features Implemented in the Source

### Content Management

- Russian and Kyrgyz article fields
- Article creation, editing and deletion
- Draft and published states
- Rubric-based content organization
- Image uploads

### Reader Experience

- Article lists and detail pages
- Search and filtering
- Pagination
- Popular-article retrieval
- Comment submission

### Administration and Moderation

- Authenticated administrative actions
- Comment approval workflow
- Public display of approved comments

Features are described from the supplied source archive,
not as a guarantee that every scenario has been tested.

## Technology Stack

| Layer | Technologies |
| :--- | :--- |
| Backend | Python, FastAPI, Pydantic |
| Database | SQLite |
| Frontend | React 18, Vite, Tailwind CSS, React Router |
| Password hashing | scrypt |
| Authentication | Custom HMAC-signed expiring bearer tokens |
| Testing tools | pytest, HTTPX, Vitest |

The archived implementation does not use Prisma or Next.js.

Its bearer token is a custom two-part signed token,
not a standard three-part JWT.

## Architecture

```text
React / Vite frontend
          |
          v
      FastAPI API
          |
          +---- SQLite
          |
          +---- Article management
          |
          +---- Administrative authentication
          |
          +---- Image uploads
          |
          +---- Comment moderation
```

## Typical Workflow

1. An authenticated editor creates a bilingual article.
2. The article is saved as a draft or published.
3. Readers browse articles using rubrics, search and pagination.
4. A reader submits a comment.
5. An editor reviews and approves the comment.
6. Approved comments are available through the public comment-list endpoint.

## Source Inventory

Static analysis of the supplied archive identified:

| Item | Count |
| :--- | ---: |
| API route decorator declarations | 18 |
| Backend test functions in test modules | 36 |

These are code-inventory counts, not evidence of successful
test execution, test coverage or production reliability.

The application and test suites were not executed during
the portfolio documentation review.

## Deployment Considerations

The archived implementation contains development defaults
and requires further review before production use:

- Replace token-signing and initial administrator defaults
- Restrict CORS to intended frontend origins
- Review authentication rate limiting
- Validate uploaded file contents and enforce appropriate limits
- Review SQLite concurrency and backup requirements
- Verify authorization and moderation behavior
- Protect credentials and private database contents

## Source Availability

Application source code, credentials, database files
and private user data are not included in this repository.

Public installation instructions are not provided because
the source code is private.

## Author and Contact

**Kubanychbek Duishekeev**  
Python Backend & AI Developer · Bishkek, Kyrgyzstan

[GitHub](https://github.com/minbaevv) ·
[LinkedIn](https://www.linkedin.com/in/kubanychbek-duishekeev-7b9872427/) ·
[Telegram](https://t.me/d_kubanychbek) ·
[Gmail](mailto:duishekeevkubanychbek@gmail.com)
