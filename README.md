# WorkForce360 — Prompt Wars 2026

A responsive workforce-management website prototype for two operational domains:
- **Airport WMS** — airport workforce operations
- **FleetForce** — delivery, transport and warehouse workforce operations

## What is included
- Responsive marketing homepage with a polished SaaS-style dashboard preview.
- Separate airport and delivery solution cards with domain-specific details.
- Feature overview, workflow section, safety and transparency section.
- Interactive sign-in and access-request dialogs.
- Mobile navigation, keyboard Escape support, reduced-motion support.
- Dockerfile configured for **Google Cloud Run** using Nginx on port 8080.
- No Python installation is required to build or deploy this static prototype.

## Important prototype limitation
This is a **front-end prototype**, not a production workforce management backend. Sign-in and access-request forms explain their demo status and do not authenticate users or save/send private data. Employee records, database, secure sessions, role-based permissions, payslip records, persistent task updates and real QR attendance are not implemented. Do not describe these as production-ready features in your submission. A full secure version would need a backend, database, authentication and server-side authorization.

## Run locally on a Mac (no Python needed)
1. Unzip the project.
2. Double-click `index.html` to preview in Safari or Chrome.
3. For a more realistic local server, install Docker Desktop only if you already have it; then run:
   ```bash
   docker build -t workforce360 .
   docker run --rm -p 8080:8080 workforce360
   ```
4. Visit `http://localhost:8080`.

## Prompt Wars submission requirements (from the provided guide)
You need all three deliverables:
1. **Public GitHub repository URL ending in `.git`**.
2. **Live Google Cloud Run URL**. Vercel and Netlify links are not accepted as the final host.
3. **Public LinkedIn post URL** explaining the problem, what you built and how it solves the problem.

The guide also specifies: public repository, exactly one branch, repository size strictly under 10 MB, login to the Innovator Dashboard using the email registered for the hackathon, paste the three links into the corresponding fields, then verify the dashboard shows the submission as recorded. Maximum two attempts; the latest submission score replaces the previous score.

## Submission steps

### A. Create a GitHub repository
1. Go to https://github.com/new and sign in.
2. Repository name: `workforce360`.
3. Set visibility to **Public**.
4. Create the repository with **no README/license/gitignore** (the project already contains these files).
5. On your Mac, open Terminal in the unzipped `WorkForce360` folder.
6. Run these commands:
   ```bash
   git init
   git add .
   git commit -m "Build WorkForce360 prototype"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/workforce360.git
   git push -u origin main
   ```
   Replace `YOUR-USERNAME` with your GitHub username. Git is usually available on a Mac; if Terminal asks to install command-line developer tools, follow the macOS prompt.
7. The GitHub repository page is the browser link, but the **submission field must use the clone URL ending in `.git`**, such as `https://github.com/YOUR-USERNAME/workforce360.git`.
8. Confirm the repository is public and only the `main` branch exists. Keep the repository under 10 MB.

### B. Deploy to Google Cloud Run (required final host)
This project uses a Dockerfile and Nginx; Python is not needed.
1. Open https://console.cloud.google.com/ and sign in to a Google account.
2. Create or select a Google Cloud project. Enable billing if Google Cloud requires it for your project; review any costs before proceeding.
3. Enable the Cloud Run and Cloud Build APIs if prompted.
4. In Google Cloud Console, open **Cloud Run** and choose **Create service** or the option to deploy a new application from source/repository (labels can vary).
5. Connect the public GitHub repository and select the `main` branch.
6. If asked how to build, choose the Dockerfile/build-from-source option so Cloud Build uses the included `Dockerfile`.
7. Set the service name to `workforce360`, choose a region, and allow unauthenticated access so evaluators can open the public demo.
8. Deploy and wait for the build to finish. Open the generated `https://...run.app` URL and test it on desktop and mobile.
9. If your console offers only a source-repository setup path, follow the current Cloud Run wizard prompts; the key requirement is that the resulting public URL is hosted on **Google Cloud Run**.
10. Do not submit a Vercel or Netlify URL.

### C. Publish the LinkedIn post
1. Create a public LinkedIn post.
2. State the problem: workforce information is split across shifts, attendance, tasks and safety reporting, with different needs across airport and delivery operations.
3. Explain the build: WorkForce360, a responsive prototype with two domain-specific experiences, built with HTML, CSS, JavaScript and a Dockerfile for Cloud Run.
4. Connect the solution to the problem and be transparent that this version is a front-end prototype.
5. Publish the post and copy the public URL to that post.

Suggested post:
> I built WorkForce360 for Prompt Wars 2026 — a workforce-management prototype designed around two operational environments: Airport WMS and FleetForce for delivery teams. The goal is to make workforce workflows easier to understand by bringing shift visibility, attendance concepts, safety reporting and task coordination into a clear, responsive interface. The project uses HTML, CSS and JavaScript, with a Dockerfile prepared for Google Cloud Run deployment. This submission is a front-end prototype, and secure authentication and persistent backend workflows are future development steps. #PromptWars2026 #ACMSRMIST #WebDevelopment

### D. Submit through Innovator Dashboard
1. Open the Innovator Dashboard provided by the hackathon organizers.
2. Sign in using the **same email address registered for the hackathon**.
3. Paste:
   - **GitHub:** `https://github.com/YOUR-USERNAME/workforce360.git`
   - **Deployed link:** the public Cloud Run URL ending in `run.app`
   - **LinkedIn post:** the public URL to your published post
4. Submit/save and verify the dashboard confirms that the submission is recorded.
5. Check all links in a private/incognito browser window to confirm public access.

## Final checklist
- [ ] GitHub repository is public and URL ends with `.git`
- [ ] Only one branch exists
- [ ] Repository is strictly below 10 MB
- [ ] Cloud Run URL is public and opens successfully
- [ ] No Vercel or Netlify URL used as final hosting
- [ ] LinkedIn post is public and explains problem, build and solution fit
- [ ] Innovator Dashboard uses the registered hackathon email
- [ ] All three links entered in the correct fields
- [ ] Dashboard confirms the submission was recorded
- [ ] Be cautious with the second attempt: latest score replaces earlier score; maximum two attempts

## Resources
- GitHub: https://github.com/
- Create repository: https://github.com/new
- Google Cloud Console: https://console.cloud.google.com/
- Cloud Run documentation: https://cloud.google.com/run/docs
- LinkedIn: https://www.linkedin.com/
