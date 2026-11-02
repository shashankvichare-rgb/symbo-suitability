# Symbo Suitability Demo — deployment steps

This folder is ready for a static Webflow Cloud deployment. The form posts directly to the deployed Google Apps Script endpoint, and the powered-by Symbo logo reference has been repaired.

## 1. Test before uploading

1. Double-click `index.html` and confirm the powered-by Symbo logo appears under the title.
2. Fill the form using clearly marked test details and submit it.
3. Open the personal-Gmail-owned Google Sheet and confirm a row appears in the `Responses` tab.

## 2. Upload to GitHub

1. Sign in to GitHub and create a new **private** repository named `symbo-suitability-demo`.
2. In the empty repository, choose **Add file → Upload files**.
3. Upload `index.html` and `webflow.json` from this folder to the repository root. `README.md` is optional.
4. Commit to the `main` branch.
5. Confirm that `index.html` and `webflow.json` are visible at the top level of the repository—not inside another folder.

## 3. Connect the repository to Webflow Cloud

1. Open the Webflow dashboard and select the existing Symbo site.
2. Open **Webflow Cloud** and create a new app/project.
3. Connect GitHub and authorize access to `symbo-suitability-demo`.
4. Select the `main` branch and the existing Symbo Webflow site.
5. Create the production environment with mount path `/solutions/suitability-demo`.
6. Deploy.
7. Visit `https://symbo.co/solutions/suitability-demo`.
8. Submit one final test form and confirm the response appears in the Google Sheet.

## Safety notes

- Do not use `/` or `/solutions` as the mount path.
- Do not create a Webflow Designer page with the exact `/solutions/suitability-demo` path.
- The Cloud app only takes over its exact mount path and descendants; the rest of the Designer site remains unchanged.
- For future page updates, replace `index.html` in the repository and commit to `main`.
