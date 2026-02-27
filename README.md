# NGA Digital Platforms Documentation

This repo houses the user guides for NGA digital platforms which can be found at [nga-digital-platforms-user-guide.netlify.app/](https://nga-digital-platforms-user-guide.netlify.app/). It is built on [MkDocs](https://www.mkdocs.org/) using an adaption of the [Material theme](https://squidfunk.github.io/mkdocs-material/).
 
This project uses [Decap CMS](https://decapcms.org/), allowing content to be edited in a browser interface. 

## 📚 Project Overview

This project provides structured documentation using:

- **MkDocs** — static site generator for documentation
- **Markdown** — simple content authoring format
- **Decap CMS** — browser-based content editing
- **Netlify** — hosting + build + CMS backend

It is designed so that:

- Developers can run and test locally
- Contributors can edit content through the CMS
- Deployment is automated through Netlify

## 🧰 Requirements

You will need:

- Python 3.9+
- pip
- git

Optional but recommended:

- virtualenv or venv
- GitHub Codespaces (for cloud dev environment)

## 🚀 Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/NGA-Digital/mkdocs-documentation-site.git
cd mkdocs-documentation-site
```

### 2. Setup virtual environment
It's a good idea to setup a virtual environment when running this project. To learn how to do this, freeCodeCamp have a [good walkthrough](https://www.freecodecamp.org/news/how-to-setup-virtual-environments-in-python/) of the process.

To launch the venv, run `source env/bin/activate`

### 3. Install dependencies
`pip install -r requirements.txt`

### 4. Run local dev server
`mkdocs serve`
If your local dev server doesn't automatically reload, use `mkdocs serve --livereload`

The site should auto reload when markdown files change.

## 🗂 Project Structure
```
docs/                → markdown content
mkdocs.yml           → mkdocs configuration
netlify.toml         → Netlify build config (optional)
static/admin/        → Decap CMS config
requirements.txt     → python dependencies
```

## Deployment
The site is deployed via Netlify.

Login credentials are: 
- Username: digital@nga.gov.au
- Password: credentials are in LastPass

All commits to main branch as well as edits via the CMS automatically triggers a deployment on Netlify.

## Content editing via CMS
This project includes Decap CMS to allow browser-based editing.

To access the CMS, go to `/admin`. 

The admin login page is `docs/admin/index.html`.

Decap CMS config file is `docs/admin/config.yml`.

Detailed information about Decap config can be found at the [config documentation page](https://decapcms.org/docs/configuration-options/).

### 👥 CMS Users

CMS user accounts are managed via Netlify Identity, which provides:
- User authentication (login/logout)
- Invitation-based user creation

#### Inviting Editors
1. Go to your site dashboard on Netlify using digital@nga.gov.au.
2. Navigate to Site Settings → Identity → Invite Users.
3. Enter the editor’s email address and send an invitation.

The invited user receives an email and can create a Netlify Identity account.

Once logged in, they can access the CMS at /admin and edit content according to permissions.

#### Managing Users

- Existing users can be deactivated or deleted from the Identity panel.
- User roles can be adjusted (Editor/Admin) to control access within Decap CMS.
- Netlify Identity integrates with Git Gateway to allow CMS changes to be committed to the repository.
