# 📦 3D Packaging Viewer

An interactive, browser-based 3D viewer for product packaging — hosted entirely on GitHub Pages. No backend, no dependencies to install.

---

## 🚀 Setup (5 minutes)

### 1. Create your GitHub repo
- Go to [github.com](https://github.com) → **New repository**
- Name it anything, e.g. `packaging-viewer`
- Set it to **Public**

### 2. Add your files
Upload these two files to the repo root:

```
your-repo/
├── index.html       ← the viewer (this file)
└── model.glb        ← your 3D packaging file
```

> **Supported formats:** `.glb` (recommended), `.gltf`, `.obj`  
> `.glb` is best — it bundles textures and geometry into one file.

### 3. Setup your Branding
Open `index.html` and find the top of the `<script>` section to set your brand name:

```js
const BRAND_NAME = 'YOURBRAND';     // ← change to your brand name
```

### 4. Enable GitHub Pages
- Go to your repo → **Settings** → **Pages**
- Under *Source*, select **Deploy from a branch**
- Choose **`main`** branch, **`/ (root)`** folder
- Click **Save**

Your viewer will be live at:
```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
```

---

## 🎮 Viewer Controls

| Action | Mouse | Touch |
|---|---|---|
| **Orbit / Rotate** | Left-click + drag | 1-finger drag |
| **Zoom** | Scroll wheel | 2-finger pinch |
| **Pan** | Right-click + drag | *(coming soon)* |
| **Reset camera** | Click ⌖ button | — |
| **Auto-rotate** | Click the badge | — |
| **Wireframe** | Click ⬡ button | — |

---

## 🎨 Customization

All customization is at the top of `index.html`:

```js
const BRAND_NAME = 'YOURBRAND';     // shown in the top-left header
```

For deeper changes, the CSS variables at the top of the `<style>` block control all colors:

```css
:root {
  --bg:      #0a0a0f;   /* page background */
  --accent:  #c8f060;   /* highlight color  */
  --accent2: #60c8f0;   /* secondary accent */
}
```

---

## 📁 Tips for your 3D file

- **GLB is recommended** — it's a single binary file with textures embedded
- If you have a `.gltf` + texture folder, export it as `.glb` from Blender, Cinema4D, or your 3D tool
- Keep file size under **25 MB** for fast loading (GitHub's limit per file)
- For files larger than 25 MB, use [Git LFS](https://git-lfs.github.com/) or host the model on a CDN and update `MODEL_URL`

---

## 🔗 Sharing

Once GitHub Pages is enabled, you can share a link to a specific model by adding `?model=filename.glb` to the end of the URL.

For example, if you uploaded `FS_Test.glb` to your repo:
```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/?model=FS_Test.glb
```

If you upload a new version of the 3D model with the same name, users just need to visit the link again. If you upload a model with a new name, you create a new link for it. 

The link works on desktop, mobile, and tablets — no app or plugin needed.
