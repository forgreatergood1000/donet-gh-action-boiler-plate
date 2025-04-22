# Hello World .NET Console App 🚀

This is a minimal **.NET Console Application** (C#) built for CI/CD demonstration using **GitHub Actions** with a reusable workflow.

---

## 📦 Project Structure

```
.
├── DotNet/ # .NET source folder
│   ├── DotNet.csproj
│   └── Program.cs
├── .github/
│   ├── workflows/
│   │   └── main.yml # Main CI workflow
│   └── actions/
│       └── build-dotnet/
│           └── action.yml # Reusable workflow
├── .gitignore
└── README.md
```

## 🚀 How to Run Locally

```bash
cd DotNet
dotnet run
```

## 🔄 GitHub Actions CI/CD

### ✅ Main Workflow

Located at: `.github/workflows/main.yml`

- **Triggers** on push to `main` or manually (`workflow_dispatch`)
- **Calls** the reusable workflow
- Passes a configurable `working-directory` input

### ♻️ Reusable Workflow

Located at: `.github/actions/build-dotnet/action.yml`

**What it does:**

- Restores NuGet packages
- Builds the app in `Release` mode
- Publishes the output to a `publish/` folder
- Uploads the output as a GitHub artifact

---

## ▶️ Run from GitHub UI

- Go to **Actions tab**
- Select the workflow
- Click **“Run workflow”**
- Enter your `.csproj` folder path (default: `DotNet`)

---

## 🛠️ Customize or Extend

- Add a `dotnet test` step
- Add Docker build and push
- Deploy to Azure, AWS, or Linux/Windows servers
- Integrate with GitHub environments (Dev → UAT → Prod)

---

> Made with ❤️ using .NET and GitHub Actions
