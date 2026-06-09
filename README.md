# 🧩 Build Fellowship — Component Library

## Development Environment Setup Guide (Storybook + Chromatic)

This guide will get your local environment ready to build a React component library using Storybook and Chromatic.

---

# 🧱 1. Prerequisites

Install the following tools before starting.

## Node.js (required)

Check if installed: 
node -v
Expected output: v18.x.x or higher (v20+ recommended) 

npm -v
Expected output: 9.x or higher


If needed, download LTS version:

[Node.js Download](https://nodejs.org/en/download?utm_source=chatgpt.com)

---

## Git (required)

### Install if needed: 

macOS: brew install git or install Xcode Command Line Tools via xcode-select --install 

Windows: Download from git-scm.com 

- In the installer, make sure to select "Add a Git Bash profile to Windows terminal” so you can use Git from the Windows terminal 

Linux: sudo apt install git (Debian/Ubuntu) or sudo dnf install git (Fedora) 


### Configure Git (first-time setup): 

git config --global user.name "Your Name" 
git config --global user.email "you@example.com"

## Code Editor (recommended)

[Visual Studio Code](https://code.visualstudio.com)

Recommended extensions:

* ESLint
* Prettier

You can use your preferred AI tools if you’d like; Cursor has a free tier. Since the goal of this project is your learning, make sure you understand the concepts and the code that is written if you use AI tools.

---

## Accounts

You will need:

* [GitHub](https://github.com)
* [Chromatic](https://www.chromatic.com)

---

# 🍴 2. Get the Starter Project

## Step 1: Fork the repository

Open:

[Component Library Starter Repo](https://github.com/amy-li-openave/component-library)

Click:

> Fork → Create your own copy

This creates your personal repo.

---

## Step 2: Clone your fork

```bash
git clone https://github.com/YOUR_USERNAME/component-library.git
cd component-library
```

---

## Step 3: Add the course repo as “upstream”

This allows you to pull updates during the course.

```bash
git remote add upstream https://github.com/amy-li-openave/component-library.git
```

Verify:

```bash
git remote -v
```

You should see:

```text
origin   → your repo
upstream → course repo
```

---

# 📦 3. Install Dependencies

Inside your project folder:

```bash
npm install
```

This installs everything needed:

* React
* TypeScript
* Storybook
* ESLint
* Chromatic integration

---

# 🚀 4. Run Storybook

Start the development environment:

```bash
npm run storybook
```

Open:

```text
http://localhost:6006
```

You should see the Storybook UI with example components.

---

# 🧪 5. Connect to Chromatic

## Step 1: Create a Chromatic project

Go to:

[Chromatic Dashboard](https://www.chromatic.com?utm_source=chatgpt.com)

* Create a new project
* Connect your GitHub repo
* Copy your project token

---

## Step 2: Add token to GitHub

In your repository:

```text
Settings → Secrets and variables → Actions → New repository secret
```

Add:

```text
CHROMATIC_PROJECT_TOKEN
```

---

## Step 3: Run Chromatic once manually

```bash
npx chromatic --project-token=YOUR_TOKEN
```

This:

* builds Storybook
* uploads it to Chromatic
* creates your visual testing baseline

---

# 🔁 6. Pulling Updates for Starter Code

When new starter code is released for our project:

Run:

```bash
git fetch upstream
git merge upstream/main
```

This updates your local project with new starter code.

---

# 📤 7. Pushing Your Work

Whenever you finish work:

```bash
git add .
git commit -m "your message"
git push origin main
```

---

# ⚙️ 8. GitHub Actions (already included)

Your repo is pre-configured with CI.

When you push:

* GitHub runs Storybook build
* Chromatic runs visual tests
* Results appear in GitHub Actions tab

You don’t need to manually configure anything.

---

# 🧪 9. Verify Everything Works

You should be able to:

### Local

```bash
npm run storybook
```

### GitHub

* push commits
* see Actions running

### Chromatic

* see published Storybook link

---

# 💡 Optional (end of course)

To make your repo portfolio-ready:

```bash
git remote remove upstream
```

This removes course linkage and makes your repo fully standalone.
