# Kamyar's Aqua Launch — Deployment

This copy of Aqua Launch is already configured for **Kamyar Fazlollahnezhad** (`@kamyarfaz`) and is intended for the separate repository:

```text
https://github.com/kamyarfaz/aqua-launch
```

Your existing `kamyarfaz/kamyarfaz` repository is not touched by this package.

> GitHub only auto-renders a profile README from a repository whose name exactly matches the username. Because `kamyarfaz/kamyarfaz` is being kept for your personal website, this Aqua Launch repository will work as a standalone showcase repository rather than automatically replacing the top of your GitHub profile.

## Publish it

1. Create a new **public** repository named `aqua-launch` under `kamyarfaz`.
2. Put the **contents of this folder** at the repository root. Keep `.github/workflows/update-profile.yml` in place.
3. Push the files to GitHub.
4. Open **Actions → Update Aqua Launch → Run workflow**.
5. If the workflow cannot push generated assets, open **Settings → Actions → General → Workflow permissions**, select **Read and write permissions**, save, and run the workflow again.

## Local preview

Python 3.10+ is recommended.

```bash
python -m pip install -r scripts/requirements.txt
python scripts/generate.py --demo
```

To request live GitHub data locally:

```bash
python scripts/generate.py
```

If local GitHub requests are rate-limited, use the GitHub Action instead. The workflow is configured to collect live data for `kamyarfaz` and refresh the generated SVG assets daily.

## Customized profile values

- GitHub: `kamyarfaz`
- Name: `Kamyar Fazlollahnezhad`
- Wordmark: `KAMYAR`
- Role: `Data Science Professional`
- Location: `Turin, Italy`
- Website: `https://kamyarfaz.com`
- Portrait: `assets/profile-source.png`
- Primary skills: Python, ML, Deep Learning, NLP / LLMs, Computer Vision, Signal Processing

Edit `config.json` later if you want to change any of these values, then rerun the generator.
