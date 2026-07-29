فلش‌کارت‌های سمانه 🌸 — Cloud Sync 2.1

Login:
- Username shown to the user: Tulipa
- Password: the password already set for the Supabase user
- Internal Supabase identity remains samaneh@tulipa.app
- Supabase session persistence is enabled, so login is normally required only once per device.

Sync:
- Local IndexedDB remains the offline copy.
- Supabase flashcard_settings.settings holds a complete cloud snapshot.
- APKG files are uploaded to the private flashcard-apkg Storage bucket.
- First login on the existing iPhone uploads existing local progress when cloud is empty.
- A new iPad with an empty library downloads the cloud snapshot and APKG files.
- Library, manual order, cards, edits, tags, suspend state, SRS/progress, positions, history, stats settings and APKGs are synchronized.
- Realtime listens for cloud snapshot updates.
- The previous IndexedDB keys are preserved so GitHub Pages updates do not reset progress.

Security:
- Only the Supabase Project URL and publishable key are embedded in the frontend.
- Never embed secret/service_role keys.
