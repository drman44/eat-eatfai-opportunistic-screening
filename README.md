# JCCT Submission Repo (One-Command Push)

This folder is a **ready-to-push GitHub repository** for the JCCT submission package.

## What’s inside
- `submission_source/` : manuscript + figures + tables (source files)
- `tools/make_submission.py` : builds a fresh submission ZIP under `submission/`
- `tools/publish.py` : **one command** to build + commit + push to GitHub
- `data/` : anonymized cohort-level features (no DICOM / no identifiers)

## One-command push (recommended)
1) Create an empty GitHub repository (no README/license) and copy its remote URL.

2) From this folder, run:

```bash
python tools/publish.py --remote <YOUR_GITHUB_REPO_URL> --msg "v0.3 initial JCCT package" --tag v0.3
```

Notes:
- Use **SSH** remote (recommended) or HTTPS remote.
- If you use HTTPS, GitHub will require a **Personal Access Token** instead of password.

## Rebuild submission ZIP anytime
```bash
python tools/make_submission.py
```

It will produce a timestamped ZIP under `submission/`.
