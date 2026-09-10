# CI/CD Pipeline: GitHub Actions → AWS S3

A static site that deploys itself. Every push to `main` triggers a GitHub
Actions workflow that syncs the site straight to an S3 bucket — no manual
upload, no console clicking, live in under a minute.

**Live site:** `http://YOUR-BUCKET.s3-website-us-east-1.amazonaws.com` *(update after deploy)*

## How it works

```
Push to main → GitHub Actions runner → AWS credentials configured
             → aws s3 sync → S3 static website → live
```

1. **Trigger** — a commit lands on `main`.
2. **Build runner** — GitHub Actions spins up a clean Ubuntu environment.
3. **Auth** — AWS credentials are pulled from encrypted GitHub Secrets, never committed to the repo.
4. **Deploy** — `aws s3 sync` pushes only the changed files to the bucket.
5. **Live** — the S3 static website endpoint serves the update immediately.

## Stack

- **GitHub Actions** — CI/CD orchestration (`.github/workflows/deploy.yml`)
- **AWS S3** — static website hosting
- **AWS IAM** — a scoped-down deploy user, credentials never touch local disk
- **GitHub Secrets** — encrypted storage for `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, `S3_BUCKET`

## Proof of a working pipeline

Five consecutive workflow runs, including two failures that were diagnosed
and fixed (a misconfigured region, then a bad commit) — the kind of thing
that happens on every real pipeline:

- ✅ GitHub Actions run history — build, fix, and deploy cycle
- ✅ Live site reflecting a content update (Day 1 → Day 2), confirming the
  auto-deploy actually works end to end

*(screenshots in `/docs` or attached to the repo's About section)*

## Running this yourself

```bash
git clone https://github.com/Ogyanframa10/YOUR-REPO-NAME.git
cd YOUR-REPO-NAME
```

1. Create an S3 bucket, enable static website hosting, and attach a public-read bucket policy.
2. Create an IAM user scoped to S3 access for this bucket, generate an access key.
3. Add `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, and `S3_BUCKET` as repo secrets under **Settings → Secrets and variables → Actions**.
4. Push to `main` — the workflow in `.github/workflows/deploy.yml` handles the rest.

## Next steps

- Front the bucket with **CloudFront** for HTTPS and a CDN
- Add a `cloudfront create-invalidation` step so cache doesn't serve stale content
- Split `develop` → staging bucket, `main` → production bucket
