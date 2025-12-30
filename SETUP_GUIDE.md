# GitHub Repository Setup Guide

## How to Upload This Repository to GitHub

**Target:** https://github.com/sshellabarger/savethehub/

---

## Option 1: Upload via GitHub Web Interface (Easiest)

### Step 1: Download from Claude
1. In this Claude conversation, download the entire `savethehub` folder
2. You should have a folder containing:
   - README.md
   - DIRECTORY.md
   - docs/ (folder)
   - data/ (folder)
   - strategy/ (folder)
   - assets/ (folder - currently empty)

### Step 2: Navigate to Your GitHub Repo
1. Go to https://github.com/sshellabarger/savethehub/
2. Click "Add file" → "Upload files"

### Step 3: Upload All Files
1. Drag the entire contents of the savethehub folder into the upload area
2. Or click "choose your files" and select all
3. GitHub will preserve the folder structure

### Step 4: Commit
1. Add commit message: "Initial commit - Save The Hub campaign materials"
2. Click "Commit changes"

**Done!** Your repository is now live.

---

## Option 2: Upload via Git Command Line (Recommended for Updates)

### Step 1: Download and Extract
Download the savethehub folder from Claude to your computer.

### Step 2: Initialize Local Repository
```bash
cd /path/to/savethehub
git init
git add .
git commit -m "Initial commit - Save The Hub campaign materials"
```

### Step 3: Connect to GitHub
```bash
git remote add origin https://github.com/sshellabarger/savethehub.git
git branch -M main
git push -u origin main
```

### Step 4: Verify
Visit https://github.com/sshellabarger/savethehub/ to confirm upload.

---

## Option 3: Clone Existing Repo and Add Files (If Repo Already Has Content)

### Step 1: Clone Your Repo
```bash
git clone https://github.com/sshellabarger/savethehub.git
cd savethehub
```

### Step 2: Copy Downloaded Files
Copy all files from the downloaded savethehub folder into your cloned repo.

### Step 3: Commit and Push
```bash
git add .
git commit -m "Add campaign documentation and financial plans"
git push origin main
```

---

## Repository Structure After Upload

```
savethehub/
├── README.md                          # Main overview (START HERE)
├── DIRECTORY.md                       # Navigation guide
├── docs/
│   ├── financing/
│   │   ├── Cooperative_Financing_Plan.md
│   │   └── Executive_Summary.md
│   ├── legal/
│   │   └── EDA_FOIA_Analysis.md
│   ├── advocacy/
│   │   └── (to be added)
│   ├── communications/
│   │   └── Winrock_Acquisition_Proposal.md
│   └── research/
│       └── Hub_History.md
├── data/
│   └── Hub_Budget_Comparison.xlsx
├── strategy/
│   └── Implementation_Timeline.md
└── assets/
    └── (images, logos to be added)
```

---

## Next Steps After Upload

### 1. **Add a Description**
On GitHub repo homepage:
- Click "Edit" (gear icon) next to "About"
- Add: "Community campaign to preserve and acquire the Arkansas Regional Innovation Hub as a member-owned cooperative"
- Add topics: `makerspace`, `cooperative`, `arkansas`, `nonprofit`, `community-ownership`
- Add website (if you create one)

### 2. **Enable GitHub Pages (Optional)**
Settings → Pages → Source: Deploy from branch (main)
- This will create a website at https://sshellabarger.github.io/savethehub/
- Great for sharing with non-technical stakeholders

### 3. **Add Collaborators**
Settings → Collaborators → Add people
- Add other campaign leadership
- Give appropriate permissions (write, admin, etc.)

### 4. **Enable Discussions**
Settings → Features → Enable Discussions
- Create categories: Announcements, Ideas, Q&A, General
- Good for community engagement

### 5. **Create Initial Issues/Projects**
Issues → New Issue
- Track to-dos (e.g., "Complete capital campaign plan")
- Assign to team members
- Set milestones

Projects → New Project
- Create project board for campaign timeline
- Track acquisition, financing, staffing phases

### 6. **Add License File (Optional but Recommended)**
Create LICENSE file:
- Creative Commons Attribution 4.0 (CC BY 4.0) recommended
- Allows others to use materials with attribution

### 7. **Add CONTRIBUTING.md (If Accepting Help)**
Create CONTRIBUTING.md with:
- How others can help
- Contribution guidelines
- Code of conduct

---

## Maintaining the Repository

### Adding New Documents
```bash
# Navigate to your local repo
cd savethehub

# Add new file to appropriate folder
# For example: docs/advocacy/Media_Strategy.md

# Stage, commit, and push
git add docs/advocacy/Media_Strategy.md
git commit -m "Add media strategy document"
git push origin main
```

### Updating Existing Documents
```bash
# Edit file locally
# Then:
git add path/to/file.md
git commit -m "Update financial projections with Q1 actuals"
git push origin main
```

### Best Practices
- **Commit often** with clear messages
- **Use branches** for major changes (create feature branch, then merge)
- **Tag releases** for major milestones (e.g., v1.0-acquisition, v2.0-relaunch)
- **Keep README updated** as campaign progresses

---

## GitHub Features to Use

### **Releases**
Create releases for major milestones:
- v1.0: Initial campaign launch
- v2.0: Acquisition complete
- v3.0: Operational launch

### **Wiki**
Enable wiki for:
- FAQs
- Glossary of terms
- Meeting notes
- Planning documents

### **Actions** (Advanced)
Set up automated workflows:
- Auto-generate PDFs from markdown
- Spell-check on commits
- Generate reports

---

## Sharing the Repository

### **Direct Link**
Share: https://github.com/sshellabarger/savethehub/

### **Specific Documents**
Link to specific files:
- README: https://github.com/sshellabarger/savethehub/blob/main/README.md
- Financing Plan: https://github.com/sshellabarger/savethehub/blob/main/docs/financing/Cooperative_Financing_Plan.md
- Etc.

### **Download Options**
Others can:
- Clone the repo: `git clone https://github.com/sshellabarger/savethehub.git`
- Download ZIP: Click "Code" → "Download ZIP"
- View online in browser

### **Embedding**
Embed README in other websites using:
```html
<iframe src="https://sshellabarger.github.io/savethehub/" width="100%" height="600"></iframe>
```

---

## Security & Privacy

### **Public vs Private**
- **Current:** Probably public (good for transparency)
- **Consider Private if:** Sensitive negotiations, confidential donor info
- **Switch anytime:** Settings → Danger Zone → Change visibility

### **What NOT to Commit**
❌ Personal contact information (phone, email - use placeholders)  
❌ Passwords or API keys  
❌ Confidential donor lists  
❌ Sensitive legal communications  
❌ Personal financial information  

✅ **Do Commit:**
- Public-facing documents
- Financial models (with sanitized data)
- Strategic plans
- Advocacy materials
- Historical research

### **.gitignore File**
Create `.gitignore` to exclude sensitive files:
```
# Sensitive files
private/
confidential/
*.private.md

# System files
.DS_Store
Thumbs.db

# Temp files
*~
*.tmp
```

---

## Troubleshooting

### **"Repository already exists" error**
Your repo exists but is empty. Use Option 3 (clone and add files).

### **Large files warning**
GitHub has 100MB file limit. If files are large:
- Use Git LFS (Large File Storage)
- Or host files elsewhere and link in README

### **Permission denied**
- Check you're logged in to correct GitHub account
- Verify you have write access to repo
- Try HTTPS instead of SSH (or vice versa)

---

## Quick Reference Commands

```bash
# Check status
git status

# Add all changes
git add .

# Commit with message
git commit -m "Your message here"

# Push to GitHub
git push origin main

# Pull latest from GitHub
git pull origin main

# Create new branch
git checkout -b feature-name

# Switch branches
git checkout main

# View commit history
git log --oneline
```

---

## Need Help?

### **Git/GitHub Resources:**
- https://docs.github.com/en/get-started
- https://git-scm.com/doc
- GitHub Desktop app (easier than command line)

### **Markdown Formatting:**
- https://www.markdownguide.org/
- Preview in VS Code, Atom, or GitHub

### **Questions?**
- GitHub Discussions in your repo
- Stack Overflow
- GitHub Support

---

## Success Checklist

After upload, verify:

- [ ] README.md displays correctly on repo homepage
- [ ] All folders (docs, data, strategy) are visible
- [ ] Files are in correct locations per DIRECTORY.md
- [ ] Links between documents work
- [ ] Hub_Budget_Comparison.xlsx opens correctly
- [ ] Repository description is set
- [ ] Topics/tags are added
- [ ] License file is added (if desired)
- [ ] .gitignore protects sensitive files

---

## What's Next?

1. **Upload these files to GitHub** (follow Option 1, 2, or 3 above)
2. **Verify everything looks good** (click through files on GitHub)
3. **Share the link** with your campaign team
4. **Start using Issues/Projects** to track work
5. **Keep updating** as campaign progresses

---

**You now have a complete, professional repository ready for your campaign!**

**Repository Link:** https://github.com/sshellabarger/savethehub/

**Questions?** Review DIRECTORY.md for navigation help or README.md for campaign overview.

---

**Last Updated:** December 30, 2025  
**Created by:** Save The Hub Campaign via Claude
