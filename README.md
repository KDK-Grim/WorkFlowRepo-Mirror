<link rel="stylesheet" type="text/css" href="custom.css">
<div align="center">
  <img  
	  src="https://raw.githubusercontent.com/KDK-Grim/WorkFlowRepo-Mirror/master/docs/ticker-bot/ticker.gif" 
  alt="Repo Ticker Stats" 
  style="height:33px;" />
  <div align="center">
  <img  
	  src="https://img.shields.io/github/stars/KDK-Grim/WorkFlowRepo-Mirror?style=social" alt="Stars"/>
  <img  
	  src="https://img.shields.io/github/forks/KDK-Grim/WorkFlowRepo-Mirror?style=social" alt="Forks"/>
  <img  
	  src="https://img.shields.io/github/last-commit/KDK-Grim/WorkFlowRepo-Mirror?style=social" alt="Last Commit"/>
</div>
  
# WorkFlowRepo-Mirror
*StatikFinTech, LLC | SFTi*

<div align="center">

  <a href="https://github.com/statikfintechllc/AscendAI/blob/master/GremlinGPT">
  <img src="https://img.shields.io/badge/Buils-passing-darkred?labelColor=black" alt="GremlinGPT Alpha"/>
  </a>
  <a href="https://github.com/statikfintechllc/AscendAI/blob/master/About Us/FOUNDER_LOG.md">
  <img src="https://img.shields.io/badge/Founder's%20Log-Manifesto-darkred?labelColor=black" alt="Founder's Log"/>
  </a>
  <a href="https://github.com/KDK-Grim/blob/master/docs/contributors.md">
  <img src="https://img.shields.io/badge/contributors-3-darkred?labelColor=black" alt="Contributors"/>
  </a>
  <a href="https://github.com/statikfintechllc/AscendAI/blob/master/About Us/FOUNDER_STATEMENT.md">
  <img src="https://img.shields.io/badge/Founder's%20Log-Statement-darkred?labelColor=black" alt="Founder's Statement"/>
  </a>
</div
<div align="center"> 
   <a href="https://github.com/statikfintechllc/WorkFlowRepo.git">
  <img src="https://img.shields.io/badge/Click%20to%20Install%20Single-Repo%20Traffic%20Workflows-darkred?labelColor=black" alt="GremlinGPT Alpha"/>
  </a>
   <a href="https://github.com/KDK-Grim/WorkFlowRepo-Mirror">
  <img src="https://img.shields.io/badge/Click%20to%20Install-Advance%20Mirror%20Workflow-darkred?labelColor=black" alt="GremlinGPT Alpha"/>
  </a>
</div>

</div>

> [!CAUTION]
>
> For these flows you need a Paid account and a Free account
> 
> Just workflows for charts, banners, and traffic data lives here.
>
> Adding more as we need them.
>
> Clone/Mirror these flows in your own Repos to show custom banners and Graphs with live data.
>
> Just change Naming Conventions to align with you're Systems.
>
> *(Instructions below)*

</div>

Use:

```bash
# Clone the repo
git clone https://github.com/KDK-Grim/WorkFlowRepo-Mirror.git
cd WorkFlowRepo-Mirror
ls
cd .github/workflows
ls
cd .. && cd ..
cd docs
ls
cd ticker-bot
ls && cd ..
cd graph
ls
cd .. && cd ..
```

> [!IMPORTANT]
>
> The above fully Installs, and Displays in terminal *ALL* folder content.
> To ensure easy navigation.

---

<details>
<summary>🔎 Expand for Setup 🔍</summary>

### 🧷 Create Both Tokens

1. Go to: `https://github.com/settings/tokens` → Fine-grained tokens  
2. Click **Generate new token**  
3. For **`PAT_GITHUB`**:
   - Scope your **current workflow free account**
   - Permissions:  
     - ✅ `Contents`: Read & Write  
     - ✅ `Metadata`: Read-only  
4. For **`PULL_STATIK_PAT`**:
   - Same as `PAT_GITHUB`, but in your paid public repo(s), to Scope your public repo(s):
     - Permissions:  
     - ✅ `Contents`: Read-only  
     - ✅ `Metadata`: Read-only  
5. Copy both tokens into thier repective Secrets

---

### 🔒 Save Tokens as Repo Secrets

In your **mirror repo** (e.g. `KDK-Grim/WorkFlowRepo-Mirror`):

- Go to: `Settings` → `Secrets and variables` → `Actions`
- Click → **New repository secret**

Add both:

```text
Name: PAT_GITHUB
Value: <your free github write token>

Name: PULL_STATIK_PAT
Value: <your paid read-only token>
```

---

## 🧬 STEP 3: Edit Workflow .yml Files

1.    Find and update Line 28 & 31 inside the traffic_graph.yml workflow file change:

```yml
- name: Fetch traffic from AscendAI
...
    REPO: statikfintechllc/AscendAI
```

> Change to match you're repo's naming.
>
> Never swap or combine these tokens.
> PAT_GITHUB is for commits.
> PULL_STATIK_PAT is for pulling public stats.

---

## 🗃️ Files to Modify:

### Inside .github/workflows, line 8 in both .yml files, ensure:

```yml
on:
  schedule:
  #  - cron: "*/5 * * * *" # Doesnt run
```

**Looks like:**

```yml
on:
  schedule:
    - cron: "*/5 * * * *" # runs every 5 minutes
```

### Inside docs/ticker-bot/fetch_stats.py, Update lines 9-16:

```python
REPOS = [
    "statikfintechllc/AscendAI",
    "statikfintechllc/Mobile-Developer",
    "statikfintechllc/AscendDocs-of-GovSeverance",
    "statikfintechllc/GodCore",
    "statikfintechllc/AscendNet",
    "statikfintechllc/WorkFlowRepo"
]
```

> Change to match you're repo's naming.

## 🔐 Using Dual Tokens Across Repositories

To fetch data **from one repo (StatikFinTech)** while committing changes **to another (your fork or mirror)**, you must use **two distinct GitHub secrets**:

| Secret Name       | Required In Repo | Permissions       | Purpose                                                  |
|-------------------|------------------|-------------------|----------------------------------------------------------|
| `PAT_GITHUB`      | ✅ Your Repo      | `contents: write` | Allows **committing/pushing** output files (graph, gif) in `<your-free-account-repo>`  |
| `PULL_STATIK_PAT` | ✅ Your Repo      | `contents: read`  | Allows **pulling traffic stats** from `<your-paid-account-repo>` |


</details>

---

<details>
<summary>🌀 Expand to See Options 🌀</summary>

---

<div align="center">

The Ticker-Bot

 ---

  <a href="https://raw.githubusercontent.com/statikfintechllc/AscendAI/master/About US/">
  <img  src="https://raw.githubusercontent.com/KDK-Grim/WorkFlowRepo-Mirror/master/docs/ticker-bot/ticker.gif" 
  alt="Repo Ticker Stats" 
  style="height:33px;" />
  </a>
</div>

---

<div align="center">

The Graph

 ---
 
  <a href="https://raw.githubusercontent.com/statikfintechllc/AscendAI/master/About US/">
  <img src="https://raw.githubusercontent.com/KDK-Grim/WorkFlowRepo-Mirror/master/docs/graph/traffic_graph.png" alt="Traffic Graph" />
  </a>
</div>

</details>

<div align="center">
  <a href="https://ko-fi.com/statikfintech_llc">
  <img  
	  src="https://img.shields.io/badge/Sponsor%20SFTi%20on%20KoFi-darkred?style=for-the-badge&logo=dragon&logoColor=gold" alt="Support"/>
  </a>
  <a href="https://patreon.com/StatikFinTech_LLC?utm_medium=unknown&utm_source=join_link&utm_campaign=creatorshare_creator&utm_content=copyLink">
  <img  
	  src="https://img.shields.io/badge/Sponsor%20SFTi%20on%20Patreon-black?style=for-the-badge&logo=dragon&logoColor=gold" alt="SFTi"/>
  </a>
</div>
<div align="center">

[![Sponsor 💪 statikfintechllc](https://img.shields.io/badge/Sponsor%20SFTi%20on%20GitHub-darkred?logo=github&style=for-the-badge)](https://github.com/sponsors/statikfintechllc)

</div>

---

*Enjoy!*
