# 祥茂光電 Engineering Knowledge Portal

Internal knowledge portal hosted on GitHub Pages.

---

## 🚀 Step 1 — Upload Documents to Google Drive

1. Open **Google Drive** → `New` → `New Folder`, name it `Engineering-Docs`
2. Inside, create sub-folders and upload your files:

   | Folder Name       | Contents                              |
   |-------------------|---------------------------------------|
   | `FlexDCA-UG`      | Entire `Parts_file.zip` (unzipped)   |
   | `IEEE`            | `IEEE802.3bm-2015.pdf`               |
   | `Python-Scripts`  | Your Python / Excel scripts          |
   | `RD-Reference`    | 研發處 TW reference documents        |
   | `EXFO-Video`      | 800G DVT videos                      |

3. For **each folder or file** you want to link:
   - Right-click → **Share** → **Anyone with the link** → **Viewer**
   - Click **Copy link**

4. Paste each link into `webhomepage.html` replacing the placeholder text:
   ```
   PASTE_GOOGLE_DRIVE_LINK_FLEXDCA   → FlexDCA folder link
   PASTE_GOOGLE_DRIVE_LINK_IEEE      → IEEE PDF link
   PASTE_GOOGLE_DRIVE_LINK_PYTHON    → Python scripts folder link
   PASTE_GOOGLE_DRIVE_LINK_RD        → R&D reference folder link
   PASTE_GOOGLE_DRIVE_LINK_EXFO      → EXFO video folder link
   ```

---

## 🐙 Step 2 — Create GitHub Repository

1. Go to [github.com](https://github.com) → **Sign in** (or create an account)
2. Click **`+`** (top right) → **New repository**
3. Settings:
   - Repository name: `engineering-portal`  (or any name)
   - Visibility: **Private** (recommended for company docs) or Public
   - ✅ Add a README file
4. Click **Create repository**

---

## 📁 Step 3 — Upload Your Files

### Option A — GitHub Web UI (easiest)
1. Open your new repository
2. Click **Add file** → **Upload files**
3. Drag and drop `webhomepage.html` (and optionally `README.md`)
4. Scroll down → **Commit changes**

### Option B — Git command line
```bash
git clone https://github.com/YOUR_USERNAME/engineering-portal.git
cd engineering-portal
cp /path/to/webhomepage.html ./index.html
git add .
git commit -m "Add homepage"
git push
```
> ⚠️ Rename `webhomepage.html` → `index.html` so GitHub Pages serves it as the root page.

---

## 🌐 Step 4 — Enable GitHub Pages

1. In your repository → **Settings** tab
2. Left sidebar → **Pages**
3. Under **Source**: select **Deploy from a branch**
4. Branch: `main` | Folder: `/ (root)`
5. Click **Save**
6. Wait ~1 minute, then your site is live at:
   ```
   https://YOUR_USERNAME.github.io/engineering-portal/
   ```

---

## ✏️ Step 5 — Future Updates

To update the page later:
1. Edit `index.html` directly on GitHub (pencil icon) **or** push via Git
2. GitHub Pages automatically redeploys within ~1 minute

---

## 📋 File Checklist

```
engineering-portal/
├── index.html        ← renamed from webhomepage.html
└── README.md         ← this file
```

All large documents (PDFs, videos, Excel, HTML help) stay on **Google Drive**.
Only the HTML page lives on GitHub.

---

## ⚠️ Notes

- The **HR Portal** link (`twhrportal.ao-inc.home`) is an internal intranet URL — it only works when connected to the company network (VPN or office).
- Google Drive "Anyone with the link" means anyone who has the URL can view — suitable for internal sharing but not fully private. For stricter access, share with specific Google accounts only.
- PyScript loads a Python runtime in the browser (~5MB) — first load may be slow.
