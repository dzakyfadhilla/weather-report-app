# Quick Setup Guide untuk SonarCloud

## ✅ Komponen yang sudah dikonfigurasi:

### 1. GitHub Actions Workflow (`/.github/workflows/ci.yml`)
- ✅ Job SonarCloud ditambahkan
- ✅ Dependency: needs `[lint, test]`
- ✅ Environment variables: `GITHUB_TOKEN` & `SONAR_TOKEN`

### 2. SonarCloud Configuration (`/weather-report/sonar-project.properties`)
- ✅ Project key: `BINAR-Learning_demo-repository`
- ✅ Organization: `binar-learning`
- ✅ Source folder: `source`
- ✅ Exclusions configured

### 3. Package.json Scripts
- ✅ `test:coverage` script added
- ✅ Build and lint scripts ready

### 4. Gitignore
- ✅ `.scannerwork/` added to ignore SonarCloud temp files

## 🔧 Setup yang masih diperlukan:

### 1. SonarCloud Account Setup
1. Login ke [SonarCloud](https://sonarcloud.io/) dengan GitHub
2. Import repository: `BINAR-Learning/demo-repository`
3. Set organization: `binar-learning`

### 2. GitHub Secrets
Tambahkan di GitHub repository → Settings → Secrets:
- `SONAR_TOKEN`: Token dari SonarCloud project settings

## 🚀 Workflow Execution Order:
```
lint → test (Node 18, 20) → sonarcloud
```

Setelah setup selesai, push ke branch `main` akan menjalankan analisis SonarCloud otomatis!
