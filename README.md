# KIDS & KIKU

Welcome to the KIDS & KIKU repository! This repository is set up with automated workflows and security features.

## How It Works

This repository includes several automated features powered by GitHub Actions:

### 🤖 AI Issue Summarization

When a new issue is created, the repository automatically:
1. Analyzes the issue title and body
2. Uses AI inference to generate a concise one-paragraph summary
3. Posts the summary as a comment on the issue

This helps contributors quickly understand new issues at a glance.

**Workflow:** `.github/workflows/summary.yml`

### 🔒 Security Scanning

The repository is equipped with CodeQL Advanced security scanning that:
- Runs automatically on pushes to the `main` branch
- Scans all pull requests targeting the `main` branch
- Performs weekly scheduled scans (every Monday)
- Analyzes code for potential security vulnerabilities

**Workflow:** `.github/workflows/codeql.yml`

## Repository Structure

```
.
├── README.md                      # This file - project documentation
├── SECURITY.md                    # Security policy and vulnerability reporting
├── .github/
│   ├── FUNDING.yml               # Funding and sponsorship configuration
│   └── workflows/
│       ├── summary.yml           # AI-powered issue summarization
│       └── codeql.yml            # Security code scanning
```

## Getting Started

1. **Create an Issue**: When you open a new issue, the AI will automatically provide a summary
2. **Security**: Review `SECURITY.md` for information about supported versions and reporting vulnerabilities
3. **Contributing**: All code contributions are automatically scanned for security issues

## Workflows in Detail

### Issue Summary Workflow
- **Trigger**: When an issue is opened
- **Permissions**: Write access to issues, read access to AI models and repository contents
- **Action**: Generates and posts an AI-powered summary of the issue

### CodeQL Security Workflow
- **Trigger**: Push to main, pull requests to main, or weekly schedule
- **Purpose**: Detect security vulnerabilities and code quality issues
- **Coverage**: Comprehensive analysis of repository code

## Support

For security concerns, please refer to our [Security Policy](SECURITY.md).

For funding and sponsorship options, see [FUNDING.yml](.github/FUNDING.yml).
