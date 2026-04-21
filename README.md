# ASAP AC and Appliance

Production-ready Vite + React landing page for `acbossinstall.com`.

## Local development

```bash
npm install
npm run dev
```

## Production build

```bash
npm run build
```

## Deploying with GitHub Pages

1. Push this repository to GitHub.
2. In GitHub, open `Settings -> Pages`.
3. Set the build source to `GitHub Actions`.
4. Push to `main` to trigger `.github/workflows/deploy.yml`.

## Exact DNS setup for `acbossinstall.com` and `www.acbossinstall.com`

These instructions assume the GitHub account serving Pages is `citygangsix`.

### Apex domain: `acbossinstall.com`

Create these four `A` records for the root domain (`@`):

```text
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

### WWW domain: `www.acbossinstall.com`

Create this `CNAME` record:

```text
Host: www
Value: citygangsix.github.io
```

### GitHub Pages custom domain

1. Leave `public/CNAME` set to `acbossinstall.com`.
2. In `Settings -> Pages`, set the custom domain to `acbossinstall.com`.
3. Wait for GitHub to verify DNS, then enable `Enforce HTTPS`.

With the `A` records on the apex domain and the `www` CNAME pointing to `citygangsix.github.io`, GitHub Pages will serve `acbossinstall.com` and support `www.acbossinstall.com` as well.
