**# 👋 Welcome to Tikipal

**Building technology that connects businesses, people, and opportunities.**

Tikipal is a technology-driven company focused on building digital solutions that simplify commerce, empower businesses, and create better experiences for people.

We believe in using technology to solve real-world problems, build scalable products, and make digital commerce more accessible.

## 🚀 What We Build

Our engineering team works across different areas of technology:

- **Backend Engineering:** Scalable APIs, business logic, and distributed systems.
- **Frontend Engineering:** Modern, intuitive, and responsive user experiences.
- **Infrastructure & DevOps:** Reliable deployments, automation, and cloud infrastructure.
- **Integrations:** Connecting platforms, services, and third-party systems.
- **Data & Automation:** Building smarter workflows and data-driven solutions.

## 👩‍💻 Engineering at Tikipal

We value:

- Clean, maintainable, and scalable code.
- Collaboration and knowledge sharing.
- Continuous learning and improvement.
- Pragmatic engineering decisions.
- Security, reliability, and performance.

## 🤝 Contributing

We believe great products are built through collaboration.

If you're part of the Tikipal engineering team, make sure to:

1. Follow the contribution guidelines of each repository.
2. Write clear commit messages and meaningful pull requests.
3. Include tests whenever possible.
4. Document important technical decisions.
5. Review code with respect and constructive feedback.

## 📚 Resources

- Check each repository's `README.md` for setup and documentation.
- Follow the contribution guidelines before submitting changes.
- Use GitHub Issues and Pull Requests to discuss technical improvements.

## 🌱 Keep Building

Technology evolves, and so do we.

We're constantly learning, experimenting, and building better solutions.

**Let's build something great together. 🚀**

---

<sub>© Tikipal · Engineering Team</sub>
**# Tikipal

**Ticketing and venue management for Colombia.**
Promoters manage their spaces and events, sell tickets with QR entry, and reach their audience by email and WhatsApp. Buyers find events and pay in the marketplace.

## Repositories

| Repo | What it is | Stack | Base branch |
|------|------------|-------|-------------|
| [Tikipal](https://github.com/Tikipal/Tikipal) | Core API, background jobs and shared identity | Django 5.2 · DRF · PostgreSQL · Redis · Celery | `develop` |
| [tikipal-business](https://github.com/Tikipal/tikipal-business) | Promoter panel: spaces, events, sales, attendees | Next.js | `development` |
| [tikipal-frontend](https://github.com/Tikipal/tikipal-frontend) | Marketplace: browse events, checkout, tickets | Next.js | `development` |

The Web3 service (NFT tickets, vaults) lives in `Tikipal/web3` (Node.js).

## How it fits together

- **One account, one email.** The API owns users and passwords. Business signs in with JWT cookies, the marketplace with Firebase. Both verify email with a one-time code.
- **The fronts never expose keys.** Browser calls go through each app's server routes (`pages/api`), which talk to the API.
- **Payments** go through Payzen. The API confirms each payment from the signed IPN, never from the browser.

## Working here

1. Start from the base branch of each repo (`develop` for the API, `development` for the fronts).
2. Changes that span repos (auth, checkout) use the same branch name in every repo, and each PR links the others.
3. Every PR passes CI: tests, lint and migrations in the API; type check and tests in the fronts.
4. Read the repo's `AGENTS.md` before you start: setup, commands and the rules that must not break.
5. Never commit secrets, and never log personal data (emails, IDs, phone numbers, payment payloads).

## Getting started

Each repo's `AGENTS.md` and `README.md` cover local setup. For anything about login or accounts, start with [Tikipal/AGENTS.md](https://github.com/Tikipal/Tikipal/blob/develop/AGENTS.md).

---

<sub>© Tikipal · Engineering</sub>
