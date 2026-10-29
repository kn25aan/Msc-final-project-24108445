# MSc Final Project

This template holds your project notebook (`MSC_final_project.ipynb`). You build your work step by step, and your supervisor can see how it develops.

## 1. Create your own repository

1. **Log in to GitHub** at <https://github.com> (create a free account with your university email if you don't have one).
2. In the top right corner, click **Use this template → Create a new repository**.
3. Set **Owner** to your account, name it e.g. `msc-project-yoursurname`, choose **Private**, and click **Create repository**.
4. **Add your supervisor as a collaborator:** **Settings → Collaborators → Add people**. Your supervisor cannot review your work without this access.

## 2. Install the tools (once)

**Anaconda (Python and Jupyter)**
Download and install from <https://www.anaconda.com/download>. Use the default options.

**Git (command line)**
- **Windows:** install from <https://git-scm.com/download/win> (default options).
- **macOS:** open Terminal and run `xcode-select --install`.

Check that it works, then tell Git who you are:

```bash
git --version
git config --global user.name "Your Name"
git config --global user.email "your.email@herts.ac.uk"
```

> Use **Anaconda Prompt** on Windows or **Terminal** on macOS for all the commands below.

## 3. Clone your repository

On your repository page, click **Code** and copy the HTTPS link. Then run:

```bash
git clone https://github.com/your-username/msc-project-yoursurname.git
cd msc-project-yoursurname
```

If Git asks you to sign in, follow the browser window. If it asks for a password, use a GitHub **personal access token** (GitHub → Settings → Developer settings → Personal access tokens), not your normal password.

## 4. Create your Python environment (once)

```bash
conda create -n msc-project python=3.11 -y
conda activate msc-project
conda install -y jupyter pandas matplotlib
```

Install any other package you need the same way, e.g. `conda install -y scikit-learn`.

## 5. Start working (every time)

```bash
conda activate msc-project
cd msc-project-yoursurname
jupyter notebook
```

Jupyter opens in your browser. Open **`MSC_final_project.ipynb`**.

## 6. Save your progress (after every task or change)

Commit and push after every task, after every change, and whenever you change an existing solution:

```bash
git status
git add .
git commit -m "CODE: what you did"
git push
```

Develop at least two parts of your project on their own branches. The notebook shows how (*Working on a branch*).

## 7. Create a release before you submit (IPR and FPR)

A release is a named snapshot of your work. It shows your supervisor exactly what you submitted.

1. Commit and push your final work.
2. On your repository page, click **Releases → Draft a new release** (or **Create a new release**).
3. Click **Choose a tag**, type `IPR-v1.0` (later `FPR-v1.0`) and click **Create new tag**. Target: `main`.
4. **Title:** e.g. *Interim Progress Report*. **Description:** 3–5 lines on what is included and what is still to do.
5. Attach your submitted **PDF** (for the FPR, also your code **.txt**).
6. Click **Publish release**.
7. Write the release name in `\gitrelease{...}` on your report's cover page, then submit on Canvas.

> Keep the repository **private**. Never commit personal data. Do not delete the repository or rewrite its history. Canvas is the official submission.
