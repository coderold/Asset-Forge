# 🛠️ AssetForge

**AssetForge** is a full-stack, developer-first asset pipeline built to solve real-world game development pain points—specifically, large third-party binary bloat and Git LFS merge conflicts across feature branches. 

Inspired by cloud review tools like Frame.io and configuration managers like Infiscal, AssetForge separates heavy master assets from your main repository history, providing a seamless web-managed cloud vault with on-demand local caching inside Unity.

---

## 🚀 Key Features

* **Cloud-Backed Repository:** Centralize heavy assets (3D models, textures, audio packs) in cloud object storage (AWS S3 / Supabase) managed through a secure backend.
* **Unity Editor Extension (`Window > AssetForge`):** Custom-built IMGUI/UI Toolkit workspace allowing developers to authenticate, browse cloud directories, and import assets directly into active project paths.
* **Smart Local Caching Engine:** Automatically caches downloaded assets locally (`AppData`) to eliminate redundant cloud bandwidth usage and ensure instant, offline-capable copy-on-demand workflows.
* **Git Conflict Elimination:** Keeps bulky binary assets out of active feature branches. Only the files explicitly copied into tracked paths (e.g., `Assets/GameFeatures/`) generate Unity `.meta` files and get tracked by version control.
* **Role-Based Security & JWT Auth:** Secure token-based developer authentication mapped to specific project permissions.

---

## 🧰 Tech Stack
* **Backend:** ASP.NET Core Web API, Entity Framework Core, PostgreSQL / SQLite.
* **Client / Tooling:** C#, Unity Editor APIs (`AssetDatabase`, `EditorWindow`).
* **Cloud & Storage:** Cloud Object Storage (S3-compatible) & Supabase Auth.
