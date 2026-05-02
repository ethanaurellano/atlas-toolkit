# ATLAS Toolkit

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/accessinter/atlas-toolkit?style=social)](https://github.com/accessinter/atlas-toolkit)
[![Contributors](https://img.shields.io/github/contributors/accessinter/atlas-toolkit)](https://github.com/accessinter/atlas-toolkit/graphs/contributors)

> **Open-source patterns, tools and examples for legacy modernization** — COBOL, Delphi, BizTalk to cloud-native stacks.

Maintained by [Access International](https://access-international.dev), A Tunisian digital services company that has been modernizing legacy code since 1999. This toolkit captures the repeatable patterns we’ve identified through the delivery of more than 10 migration proof-of-concepts (35,524 lines converted).

## Why this toolkit?

Legacy modernization is a strategic initiative for thousands of companies (banks, insurance firms, the public sector, and industry). Yet every program reinvents the wheel. There is no shared catalog, few documented open-source patterns, and no common tools for demonstrating functional equivalence.

**ATLAS Toolkit opens our patterns**. Not the entire methodology (which remains proprietary), but the reusable technical building blocks: translation patterns, parity tests, migration scaffolds, and mismatch rules.

## Contenu

### `/patterns`

Documented translation patterns, including source-to-target examples and parity tests.

| Source | Target | Pattern | File |
|---|---|---|---|
| COBOL | TypeScript | PERFORM loops → forEach/for-of | [`patterns/cobol/perform-loops.md`](patterns/cobol/perform-loops.md) |
| COBOL | Java | EVALUATE → switch/case | Coming soon |
| COBOL | TypeScript | File I/O indexed → Map | Coming soon |
| Delphi | TypeScript | TStringList → Array | Coming soon |
| BizTalk | Azure Logic Apps | Orchestration XLANG → workflow.json | Coming soon |

### `/tools`

Small command-line tools for automating repetitive tasks.

| Tool | Purpose |
|---|---|
| `parity-tester` | Compare the legacy run with the target run, and identify any discrepancies |
| `discrepancy-registry` | Generates a signable discrepancy log |
| `cobol-splitter` | Break down a monolithic COBOL program into translatable modules |

### `/examples`

Complete, working examples—not stubs.

- [`examples/card-demo-cobol/`](examples/card-demo-cobol/) : CARDDEMO application (IBM sample) migrated from COBOL → TypeScript Cloudflare Worker
- More to come

### `/docs`

- [`docs/philosophy.md`](docs/philosophy.md) — Why we document these patterns
- [`docs/contributing-guide.md`](docs/contributing-guide.md) — How to propose a new pattern
- [`docs/atlas-methodology-intro.md`](docs/atlas-methodology-intro.md) — Overview of the complete methodology (introduction, without proprietary details)

## Quickstart

```bash
# Clone
git clone https://github.com/accessinter/atlas-toolkit.git
cd atlas-toolkit

# Install dependencies for the tools
cd tools/parity-tester && npm install

# Run an example
cd ../../examples/card-demo-cobol && npm install && npm test
```

## Contribute

Contributions are **welcome and encouraged**. Found a migration pattern that works? A useful tool for comparing runs? An educational example?

See [`CONTRIBUTING.md`](CONTRIBUTING.md) for detailed instructions.

**Good first issue** :
- [Issues avec label `good first issue`](https://github.com/accessinter/atlas-toolkit/labels/good%20first%20issue)

## Who uses this toolkit?

- [Access International](https://access-international.dev) (maintainer)
- *Add your business via PR — we'd love to hear from you*

## Supported target stacks

- **TypeScript** (Cloudflare Workers, Node.js, Deno)
- **Java 21** (Spring Boot)
- **.NET 8** (ASP.NET Core)
- **Python** (FastAPI, Polars pour batch)
- **Azure Logic Apps** (pour orchestrations BizTalk)

## Licence

MIT. You may use the patterns and tools in your commercial projects; attribution is not required but is appreciated.

## License

- Site : [access-international.dev](https://access-international.dev)
- Complete Methodology : [access-international.dev/fr/methodologie-atlas](https://access-international.dev/fr/methodologie-atlas)
- Contact : [access-international.dev/fr/contact](https://access-international.dev/fr/contact)
- Twitter/X : [@accessint](https://twitter.com/accessint) *(placeholder)*

---

*“The legacy systems that keep banks, insurance companies, and government agencies running are not a problem to be hidden—they are an asset to be systematically modernized.”*

# ATLAS Toolkit

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/accessinter/atlas-toolkit?style=social)](https://github.com/accessinter/atlas-toolkit)
[![Contributors](https://img.shields.io/github/contributors/accessinter/atlas-toolkit)](https://github.com/accessinter/atlas-toolkit/graphs/contributors)

> **Open-source patterns, tools and examples for legacy modernization** — COBOL, Delphi, BizTalk to cloud-native stacks.

Maintenu par [Access International](https://access-international.dev), une ESN tunisienne qui modernise du code legacy depuis 1999. Ce toolkit capture les patterns répétables que nous avons identifiés en livrant plus de 10 POC de migration (35 524 lignes converties).

## Pourquoi ce toolkit

La modernisation legacy est un chantier stratégique pour des milliers d'entreprises (banques, assurances, secteur public, industrie). Pourtant, chaque programme réinvente la roue. Pas de catalogue partagé, peu de patterns documentés en open source, aucun outillage commun pour prouver la parité fonctionnelle.

**ATLAS Toolkit ouvre nos patterns**. Pas toute la méthodologie (qui reste propriétaire), mais les briques techniques réutilisables : patterns de traduction, test de parité, scaffolds de migration, règles de discordances.

## Contenu

### `/patterns`

Patterns de traduction documentés, avec exemple source → cible + tests de parité.

| Source | Cible | Pattern | Fichier |
|---|---|---|---|
| COBOL | TypeScript | PERFORM loops → forEach/for-of | [`patterns/cobol/perform-loops.md`](patterns/cobol/perform-loops.md) |
| COBOL | Java | EVALUATE → switch/case | À venir |
| COBOL | TypeScript | File I/O indexed → Map | À venir |
| Delphi | TypeScript | TStringList → Array | À venir |
| BizTalk | Azure Logic Apps | Orchestration XLANG → workflow.json | À venir |

### `/tools`

Petits outils de ligne de commande pour automatiser les tâches répétitives.

| Outil | But |
|---|---|
| `parity-tester` | Compare run legacy vs run cible, identifie les discordances |
| `discrepancy-registry` | Génère un registre signable de discordances |
| `cobol-splitter` | Découpe un programme COBOL monolithe en modules traductibles |

### `/examples`

Exemples complets fonctionnels — pas des stubs.

- [`examples/card-demo-cobol/`](examples/card-demo-cobol/) : application CARDDEMO (IBM sample) migrée COBOL → TypeScript Cloudflare Worker
- Autres à venir

### `/docs`

- [`docs/philosophy.md`](docs/philosophy.md) — pourquoi on documente ces patterns
- [`docs/contributing-guide.md`](docs/contributing-guide.md) — comment proposer un nouveau pattern
- [`docs/atlas-methodology-intro.md`](docs/atlas-methodology-intro.md) — aperçu de la méthodologie complète (intro, sans les détails propriétaires)

## Quickstart

```bash
# Cloner
git clone https://github.com/accessinter/atlas-toolkit.git
cd atlas-toolkit

# Installer deps pour les outils
cd tools/parity-tester && npm install

# Lancer un exemple
cd ../../examples/card-demo-cobol && npm install && npm test
```

## Contribuer

Les contributions sont **bienvenues et encouragées**. Pattern de migration trouvé qui fonctionne ? Outil utile pour comparer des runs ? Exemple pédagogique ?

Voir [`CONTRIBUTING.md`](CONTRIBUTING.md) pour le process détaillé.

**Bon premiers tickets** :
- [Issues avec label `good first issue`](https://github.com/accessinter/atlas-toolkit/labels/good%20first%20issue)

## Qui utilise ce toolkit

- [Access International](https://access-international.dev) (maintainer)
- *Ajoutez votre entreprise via PR — on aime savoir*

## Stack cibles supportées

- **TypeScript** (Cloudflare Workers, Node.js, Deno)
- **Java 21** (Spring Boot)
- **.NET 8** (ASP.NET Core)
- **Python** (FastAPI, Polars pour batch)
- **Azure Logic Apps** (pour orchestrations BizTalk)

## Licence

MIT. Vous pouvez utiliser les patterns et outils dans vos projets commerciaux, sans attribution obligatoire mais appréciée.

## Liens

- Site : [access-international.dev](https://access-international.dev)
- Méthodologie complète : [access-international.dev/fr/methodologie-atlas](https://access-international.dev/fr/methodologie-atlas)
- Contact : [access-international.dev/fr/contact](https://access-international.dev/fr/contact)
- Twitter/X : [@accessint](https://twitter.com/accessint) *(placeholder)*

---

*"Le legacy qui fait tourner les banques, les assurances et les administrations n'est pas un problème à cacher — c'est un patrimoine à moderniser avec méthode."*
