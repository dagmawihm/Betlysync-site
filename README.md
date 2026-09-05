# Betlysync public information site

This repository contains Betlysync's static legal and information site for its public homepage and Google OAuth configuration. These files are GitHub Pages compatible. No build step, package manager, framework, JavaScript, or external font is required. No analytics, cookies, or tracking pixels are included.

## Files

- `index.html`: Product overview, optional Gmail connection, and intended read/send behavior.
- `privacy.html`: Privacy Policy covering account, Gmail, hosting, and service data.
- `terms.html`: Terms of Use covering the MVP, user responsibilities, and third-party services.
- `styles.css`: Shared responsive layout, typography, keyboard focus, and print styles.
- `README.md`: Local review and future publishing instructions.

## Review locally before publishing

Open `index.html` in a browser. Follow Home, Privacy, and Terms; all site navigation and stylesheet links are relative and also work under a repository URL. The site works with JavaScript disabled.

Replace every `[LEGAL OPERATOR NAME]` and `[CONTACT EMAIL]` in both legal HTML files, including their top-of-file comments, with the actual operator name and public contact email. The placeholders are highlighted in each Contact section. Do not publish with placeholders remaining.

Both legal pages use **September 4, 2026** as the effective date. Review the drafts against actual operational practices before publication, especially data collection, retention/deletion handling, security, and provider processing. No fixed retention period or self-service account deletion workflow is promised. Sending is described as functionality being added; update its availability wording when it is live. AI drafting is not presented as an existing feature.

The Privacy Policy links to the official [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including applicable Limited Use requirements. These pages alone do not establish Google OAuth approval. Ensure the actual application, consent screen, and requested scopes match the disclosures; request send access when the corresponding feature is available for use.

## Git commands after local review

The folder was not a Git repository when these files were created. Run these commands in PowerShell after filling the placeholders and reviewing the files:

```powershell
Set-Location 'E:\work\Apps\Betlysync-site'
git init -b main
git add index.html privacy.html terms.html styles.css README.md
git diff --cached --check
git diff --cached
git commit -m "Add Betlysync static information and legal site"
```

When you decide to publish, create an empty public GitHub repository without an initial README, license, or gitignore. Replace `USERNAME` and `REPOSITORY` below with its actual owner and repository name, then run:

```powershell
git remote add origin https://github.com/USERNAME/REPOSITORY.git
git push -u origin main
```

These commands are instructions only. No push or deployment was performed when creating the site.

## GitHub Pages setup (when ready to publish)

In the GitHub repository, choose **Settings → Pages → Deploy from a branch → main → /(root)**, then **Save**. See [GitHub's publishing-source instructions](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

Expected public URLs:

- Homepage: `https://USERNAME.github.io/REPOSITORY/`
- Privacy Policy: `https://USERNAME.github.io/REPOSITORY/privacy.html`
- Terms of Use: `https://USERNAME.github.io/REPOSITORY/terms.html`

Use the actual published URLs in the corresponding Google OAuth configuration fields after verifying they are publicly reachable. No custom domain is assumed or configured.
