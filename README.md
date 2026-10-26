# Botanical product clinical studies

A grouped planning workspace for pain, sleep, anxiety, and focus protocol tracks. Each indication retains its own source protocol repo and notebook example. This package is not a submitted or approved protocol, does not contain participant data, and must not be used to infer trial results.

## Reproduce the index notebook

`conda env create -f environment.yml`, activate the environment, and run `jupyter lab notebooks/analysis.ipynb`. The indication-specific example notebooks are also included.

## Source repositories

- [Pain](https://github.com/Terpedia/trial-2026-pain)
- [Sleep](https://github.com/Terpedia/trial-2026-sleep)
- [Anxiety](https://github.com/Terpedia/trial-2026-anxiety)
- [Focus](https://github.com/Terpedia/trial-2026-focus)

Each trial protocol remains separate. Resolve classification, study design, intervention, endpoints, ethics/IRB, consent, oversight, and analysis before registration or participant activity.


## Terpedia access

The optional client in `src/terpedia_access.py` calls the Terpedia Knowledge API at `/v1/tabular/search`. It reads `TERPEDIA_KNOWLEDGE_API_KEY` and `TERPEDIA_KB_API_URL` from the process environment and sends the key in the `x-knowledge-key` header. Copy `.env.example` as a configuration reference, then provide the real key through a local secret manager, Codespaces secret, or authorized GitHub Actions secret. Never commit `.env` or print the key in notebook output.
