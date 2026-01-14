
# Gemini CLI Tutorial (Windows)

A **student-friendly, step-by-step guide** to installing and using **Gemini CLI** on Windows.  
This repository helps you move from **basic chat usage** to **power-user workflows** such as:

- Reading local files directly
- Explaining code and logs
- Piping command output into Gemini
- Managing project-level AI behavior
- Automating everyday tasks

👉 Live tutorial page: **GitHub Pages (index.html)**

---

## Who This Is For

This tutorial is designed for:

- Undergraduate and graduate students
- Researchers and teaching assistants
- Beginners with no command-line background
- Anyone who wants to use Gemini beyond the browser

No prior AI or programming expertise is required.

---

## What You Will Learn

By the end of this tutorial, you will be able to:

- Install Gemini CLI correctly on Windows
- Authenticate once and reuse the session
- Use Gemini directly from PowerShell
- Read files using the `@` symbol
- Analyze command output using piping `|`
- Apply permanent project rules using `GEMINI.md`
- Run one-line automation commands

---

## Repository Structure

```text
.
├── index.html      # Main tutorial (GitHub Pages)
├── README.md       # This file
````

---

## Requirements

Before starting, make sure you have:

* Windows 10 or Windows 11
* PowerShell
* Internet connection
* Google account
* Node.js (LTS version)

---

## Quick Start (Summary)

### 1. Install Node.js

Download and install Node.js (LTS) from:
[https://nodejs.org](https://nodejs.org)

Verify installation:

```powershell
node --version
npm --version
```

---

### 2. Install Gemini CLI

```powershell
npm install -g @google/gemini-cli
```

Verify:

```powershell
gemini --version
```

---

### 3. Fix PATH (If Needed)

If `gemini` is not recognized:

```powershell
$env:Path += ";C:\Users\<YOUR-USERNAME>\AppData\Roaming\npm"
gemini --version
```

Replace `<YOUR-USERNAME>` with your Windows username.

---

### 4. Login to Gemini

```powershell
gemini auth login
```

A browser window will open.
Sign in with your Google account and approve access.

This step is usually required only once.

---

## Basic Usage

### Start interactive mode

```powershell
gemini
```

Useful commands inside chat:

```text
/clear   # Clear screen
/reset   # Reset session context
/exit    # Exit Gemini CLI
```

---

## Reading Files (Core Feature)

Gemini CLI can read files directly from your computer.

### Explain a Python script

```text
@script.py Explain this code step by step
```

### Compare two files

```text
@v1.py @v2.py What is the difference between these two scripts?
```

### Read multiple small files

```text
@*.txt Summarize these notes into one paragraph
```

⚠️ Avoid large folders or thousands of files.

---

## Piping Command Output

You can send output from PowerShell commands directly into Gemini.

### Analyze an error log

```powershell
Get-Content error.log | gemini "What caused this error and how do I fix it?"
```

### Generate a Git commit message

```powershell
git diff | gemini "Write a concise commit message"
```

### Check memory-heavy processes

```powershell
Get-Process | gemini "Which top 3 processes use the most memory?"
```

This eliminates copy-paste entirely.

---

## Project-Level Instructions (GEMINI.md)

You can define permanent instructions for a project.

### Example

1. Create a project folder:

```powershell
mkdir MyProject
cd MyProject
```

2. Create `GEMINI.md`:

```markdown
You are a strict Python code reviewer.
Always point out inefficiencies and bugs.
Be concise and practical.
```

3. Run Gemini:

```powershell
gemini
```

Gemini will now follow these rules automatically.

---

## One-Line Automation

Run a task and exit immediately:

```powershell
gemini "Write a professional email saying I will be 10 minutes late"
```

Useful for scripts and automation workflows.

---

## Student Practice Task

Try this command:

```powershell
Get-Process | gemini "Identify the top 3 memory consuming processes and explain them briefly."
```

This demonstrates:

* System integration
* Real command output analysis
* Practical AI usage

---

## Important Notes

* Gemini CLI **does not control your computer**
* It only analyzes the text you provide
* Be mindful when sharing sensitive files or logs

---

## How to Use This Repository

1. Open `index.html` locally
2. Or publish it using **GitHub Pages**
3. Share the link with students
4. Use it as a lab guide or self-study material

---

## License

This project is licensed under the MIT License.  
See the [LICENSE](LICENSE) file for details.

---
