# Overtron Digital Website — Setup Guide

Website for OVERTRON DIGITAL LTD to verify Google Play Developer organization account, host privacy policies, and showcase apps.

## Status

- [x] Website files created (homepage, app pages, privacy policies, CSS)
- [x] Git repo initialized with initial commit
- [ ] Create GitHub Organization
- [ ] Create repo under org
- [ ] Register domain
- [ ] Configure DNS
- [ ] Enable GitHub Pages
- [ ] Google Search Console verification
- [ ] Play Console website verification
- [ ] Update Play Store listing URLs
- [ ] Migration cleanup (archive old j86hughes.github.io)

---

## Step 1: Create GitHub Organization

1. Go to https://github.com/organizations/plan
2. Organization name: `overtron-digital`
3. Free plan is fine

## Step 2: Create Repo Under the Org

1. Create repo: `overtron-digital.github.io` (public, empty — no README)
2. Add remote and push:
   ```bash
   git remote add origin git@github.com:overtron-digital/overtron-digital.github.io.git
   git push -u origin main
   ```

## Step 3: Register Domain

- Domain: `overtrondigital.com`
- Any registrar (Namecheap, Cloudflare, etc.)

## Step 4: Configure DNS

Add these records at your registrar:

| Type | Name | Value |
|------|------|-------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | overtron-digital.github.io |

## Step 5: Enable GitHub Pages

1. Go to repo Settings → Pages
2. Source: Deploy from branch `main`, root `/`
3. Custom domain: `overtrondigital.com`
4. Check "Enforce HTTPS"

## Step 6: Google Search Console Verification

1. Go to https://search.google.com/search-console
2. Add property: `overtrondigital.com`
3. Choose DNS verification — add the TXT record Google provides:
   | Type | Name | Value |
   |------|------|-------|
   | TXT | @ | google-site-verification=... (value from Search Console) |
4. Wait for DNS propagation, then click Verify

## Step 7: Play Console Website Verification

1. Go to Play Console → Account Details → Organization Website
2. Enter: `https://overtrondigital.com`
3. Click "Send Verification Request"
4. If same Google account for Search Console and Play Console → auto-approved
5. If different accounts → approve via email sent to Search Console owner

## Step 8: Update Play Store Listings

### TOPIK Master
| Field | New URL |
|-------|---------|
| Privacy Policy | `https://overtrondigital.com/topik-master/privacy-policy.html` |
| Developer Website | `https://overtrondigital.com` |
| Support URL | `https://overtrondigital.com/topik-master/` |

### Dual N-Back
| Field | New URL |
|-------|---------|
| Privacy Policy | `https://overtrondigital.com/dual-n-back/privacy-policy.html` |
| Developer Website | `https://overtrondigital.com` |
| Support URL | `https://overtrondigital.com/dual-n-back/` |

## Step 9: Migration Cleanup

- Keep `j86hughes.github.io` live temporarily until AdMob re-crawls `app-ads.txt` at the new domain
- Once everything is confirmed working, archive the old repo
- Contact email on all pages: `masseffect2020@gmail.com`

---

## Site Structure

```
overtron-digital.github.io/
├── index.html                        # Homepage
├── topik-master/
│   ├── index.html                    # TOPIK Master app page
│   └── privacy-policy.html           # Privacy policy
├── dual-n-back/
│   ├── index.html                    # Dual N-Back app page
│   └── privacy-policy.html           # Privacy policy
├── css/
│   └── style.css                     # Shared styles
├── app-ads.txt                       # AdMob verification
├── CNAME                             # overtrondigital.com
└── .gitignore
```

## Key Details

| Item | Value |
|------|-------|
| Company | Overtron Digital Ltd |
| Domain | overtrondigital.com |
| GitHub Org | overtron-digital |
| Contact Email | masseffect2020@gmail.com |
| AdMob Publisher ID | pub-8482364065047846 |
| TOPIK Master Package | com.topikvocab.app |
| Dual N-Back Package | com.dualnback |
