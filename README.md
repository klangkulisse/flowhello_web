# flowhello_web

Static landing site for FloHello, prepared for deployment on Azure Static Web Apps.

## Naming convention

Use the `flowhello_` prefix for all new registrations.

- GitHub user: `klangkulisse`
- Suggested GitHub repository: `flowhello_web`
- Suggested Azure Static Web App name: `flowhello_web_prod`
- Suggested production hostname label: `flowhello_web`

This gives you a clean default pairing:

- GitHub: `https://github.com/klangkulisse/flowhello_web`
- Azure Static Web App: `flowhello_web_prod`

## Project structure

- `index.html` contains the main one-page site
- `styles.css` contains the full visual system and responsive layout
- `main.js` adds scroll reveal motion
- `staticwebapp.config.json` configures Azure Static Web Apps routing and headers
- `assets/` contains the public FloHello brand assets used by the site

## GitHub setup

If you want to publish this folder as the recommended GitHub repo, use:

```powershell
git init
git add .
git commit -m "Initial FloHello static site"
gh repo create klangkulisse/flowhello_web --public --source=. --remote=origin --push
```

If you prefer a private repo, replace `--public` with `--private`.

## Azure Static Web Apps setup

1. In Azure, create a new Static Web App named `flowhello_web_prod`.
2. Choose GitHub as the deployment source.
3. Connect the repository `klangkulisse/flowhello_web`.
4. Use these build settings:

```text
App location: /
Api location:
Output location:
```

5. Add the deployment token to the GitHub repository secret:

```text
AZURE_STATIC_WEB_APPS_API_TOKEN_FLOWHELLO_WEB
```

## GitHub Actions

The workflow at `.github/workflows/azure-static-web-apps-flowhello_web.yml` is already configured for:

- pushes to `main`
- preview environments for pull requests
- closing preview environments when pull requests are closed

## Next recommended edits

- replace the placeholder email link with your real inbox
- add the final domain once Azure is live
- add a real LinkedIn company URL
- add case studies or founder/team sections when ready
