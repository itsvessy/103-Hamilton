# Vessy Home — GitHub Pages setup

This package contains a homepage and privacy policy for your personal Nest integration. Open index.html in your browser to review both pages before publishing. The site is informational; it has no server connection, analytics code, or credentials.

## Publish on GitHub Pages

1. Sign in to GitHub as itsvessy.
2. Create a PUBLIC repository named exactly itsvessy.github.io. Add a README during creation. If that repository already exists, preserve its existing content and pause before uploading a replacement homepage.
3. In the repository, choose Add file > Upload files. Upload index.html and privacy.html into the repository root, then commit to main. Upload the extracted HTML files, not this ZIP archive. This README is for your reference and does not need uploading.
4. Open Settings > Pages. Under Build and deployment, choose Deploy from a branch, branch main, folder /(root), then Save.
5. Wait for deployment to finish. Open both public URLs below and confirm the homepage's Privacy link works. GitHub notes that publishing can take up to ten minutes.

Homepage: https://itsvessy.github.io/
Privacy policy: https://itsvessy.github.io/privacy.html

## Configure Google OAuth Branding

Sign in to Google Cloud as the owner of the existing OAuth project (your 103 account). Open that project's Google Auth Platform > Branding.

- App name: Vessy Home
- User support email: keep your existing monitored support email.
- Developer contact email: keep your existing monitored contact email.
- Authorized domains: ADD itsvessy.github.io (without https:// or a path). Preserve existing authorized domains.
- Application home page: https://itsvessy.github.io/
- Application privacy policy link: https://itsvessy.github.io/privacy.html

Save, then open Audience > Publish app and confirm. The desired Publishing status is In production. Publishing the app and publishing verified branding are separate controls. Google's personal-use exemption means mandatory OAuth scope verification is not required for this household app; an unverified-app warning can still appear.

Keep the OAuth client's existing redirect URI exactly as configured:
https://my.home-assistant.io/redirect/oauth

## If Google requests domain ownership verification

1. While signed in as the Google Cloud project owner, open Google Search Console.
2. Add a URL-prefix property: https://itsvessy.github.io/
3. Choose HTML file verification. Download the exact verification HTML file Google provides.
4. Upload that file, unchanged, beside index.html in the GitHub repository and commit it. Wait for Pages to publish it and confirm its exact verification URL opens.
5. Return to Search Console and select Verify. Leave that verification file in the repository afterwards.
6. Return to Google Auth Platform and retry saving the Branding settings and publishing from Audience.

## After publishing

Confirm Audience shows In production. A Nest authorization originally issued in Testing should not be assumed to have lost its seven-day limit: complete a fresh authorization after publishing, using the Google account that owns the Nest home (your vessys account). Use Home Assistant's reauthentication flow when available; do not delete a working integration just to force this step. If no reauthentication option is shown, continue with guided troubleshooting before changing credentials.

## Official references

- GitHub Pages creation: https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- GitHub Pages publishing: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
- Google OAuth Branding: https://support.google.com/cloud/answer/15549049
- Google personal-use verification exemption: https://support.google.com/cloud/answer/13464323
- Google site ownership verification: https://support.google.com/webmasters/answer/9008080
