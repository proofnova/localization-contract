# ICU localization gate

번역문의 중첩 ICU 인자·선택·복수형·보호 토큰 누락을 검사한다.

A focused executable resource for AI-assisted structured work. **Zero runtime dependencies, no API key, Node.js 22+.**

[Live workspace](https://proofnova.github.io/localization-contract/) · [한국어 리소스 모음](https://proofnova.github.io/) · [Task contract](resource.json) · [Prior art](RESEARCH.md)

```sh
git clone https://github.com/proofnova/localization-contract.git
cd localization-contract
npm test
node cli.mjs example.json
```

## What it does

A bounded nested MessageFormat parser rather than a flat placeholder regex.

Nested plurals and quoted literal braces must not be mistaken for missing or extra arguments.

## Connect a model

Import `execute` from `./run.mjs`. Expose this declared tool to your model, validate its tool name/input contract, execute it, and retain the returned JSON and input digest. Calculations and constraint checks are performed by the resource. No paid model or new agent framework is required.

[SKILL.md](SKILL.md) contains the workflow, interpretation and recovery procedure. [example.json](example.json) is a complete input; [cases.json](cases.json) contains worked and held-out synthetic checks. The website executes the same code locally in a bounded Worker. It has no model or external data upload.

## Recovery and limits

Repair the exact missing argument/category/brace; semantic translation review remains separate.

Underlying algorithms and task outcomes already exist in the alternatives. An existing public catalog auditor describes overlapping nested ICU checks. Small synthetic tests cannot establish broad expertise or external demand. See [RESEARCH.md](RESEARCH.md). A plan/audit is not an external action or proof of actual user benefit.

## Contribute

Open an issue with a synthetic/redacted failing JSON input, expected result and Node version. Add a regression test and run `npm test`. Never include credentials or real private records in public examples.

MIT · Proofnova · 2026
