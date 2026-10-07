# Noviai Website

Static landing page for **Noviai**.

## Local preview

Just open `index.html` in your browser, or run:

```bash
python -m http.server 8080
```

Then open:

```text
http://localhost:8080
```

---

# Deploy to GitHub in one go

## 1. Create a new empty GitHub repository

Recommended repository name:

```text
noviai-site
```

Do **not** initialize it with README, .gitignore, or license because this folder already contains files.

## 2. Open PowerShell inside this folder and run

Replace `YOUR_GITHUB_USERNAME` with your GitHub username.

```powershell
git init
git branch -M main
git add .
git commit -m "Launch Noviai website"
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/noviai-site.git
git push -u origin main
```

## 3. Enable GitHub Pages

GitHub repository → **Settings** → **Pages**

Under **Build and deployment**:

- Source: `Deploy from a branch`
- Branch: `main`
- Folder: `/ (root)`
- Click **Save**

Wait around 1–3 minutes.

GitHub will initially give you a URL similar to:

```text
https://YOUR_GITHUB_USERNAME.github.io/noviai-site/
```

---

# Connect hieuit.site

A `CNAME` file is already included and contains:

```text
hieuit.site
```

In GitHub:

**Settings → Pages → Custom domain**

Enter:

```text
hieuit.site
```

and save it.

Then go to **Cloudflare → hieuit.site → DNS → Records**.

For the root domain, GitHub Pages supports these A records:

| Type | Name | Content |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

For `www`, add:

| Type | Name | Content |
|---|---|---|
| CNAME | www | YOUR_GITHUB_USERNAME.github.io |

For the initial setup, if GitHub domain verification has trouble, set the Cloudflare proxy to **DNS only** (gray cloud). After GitHub verifies the custom domain and HTTPS is active, you can test enabling Cloudflare proxy again if desired.

Back in GitHub Pages, enable:

```text
Enforce HTTPS
```

Final website:

```text
https://hieuit.site
```

---

# Before reapplying to Claude Startups

Keep these details consistent everywhere:

- Company: `Noviai`
- Website: `https://hieuit.site`
- Email: `hua@hieuit.site`
- Founder: `Trung Hieu Hua`
- Founded: `2024`
- Location: `Ho Chi Minh City, Vietnam`
- Funding: `Bootstrapped / Not yet raised`

Edit `index.html` if any of these details are not accurate.

## Recommended extra credibility

After publishing:

1. Add `Noviai` to your LinkedIn Experience.
2. Link LinkedIn back to `https://hieuit.site`.
3. Add links to real demos or GitHub projects when they are public.
4. Keep the same company name in Claude Console and Claude Startups application.
