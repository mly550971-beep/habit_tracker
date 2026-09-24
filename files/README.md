# Habit Tracker

Offline desktop habit tracker built with **PyQt6 + matplotlib + SQLite**.
No internet, no accounts, no telemetry — all data stays on your machine.

تطبيق سطح مكتب أوفلاين لتتبع العادات، مبني بـ PyQt6 و matplotlib و SQLite. كل بياناتك بتفضل على جهازك.

<!-- Add screenshots here, e.g. ![Main window](docs/screenshot.png) -->

## Features · المميزات

- Habit table with **Month / Week** views, category filter and quick **search**
- **Check** habits and **Numeric** habits (daily goal + unit), drag & drop ordering
- Auto-suggested icon per category
- Daily **mood** + **notes**, *Review Missed Days*, *Finish Month* + yearly progress
- Stats aware of habit creation date; future days never count as missed
- Current / best **streaks**, XP, levels, achievements, daily celebration
- **Planner**: appointments, deliveries, deadlines, tasks, notebook (search, pin, categories)
- Daily reminders + system tray, alarm sound (AM/PM time controls)
- Themes: Dark / Light / Paper / Ocean, subtle animated background
- Arabic / English UI, profile with live clock by timezone

## Requirements

- Python 3.9+
- Windows, Linux or macOS (alarm sound uses `winsound` on Windows only; other systems use a system beep)

## Run

```bash
pip install -r requirements.txt
python main.py
```

## Where is my data?

The database (`habit_tracker.db`) is stored in your user data folder:

| OS | Location |
|----|----------|
| Windows | `%APPDATA%\HabitTracker\` |
| macOS | `~/Library/Application Support/HabitTracker/` |
| Linux | `~/.local/share/HabitTracker/` |

If an older `habit_tracker.db` exists next to `main.py`, it is **copied** there on first run (the original is not deleted).
Set the `HABIT_TRACKER_DB` environment variable to use a custom path.

## Build a Windows EXE

```bat
build_windows.bat
```

Output: `dist\HabitTracker\HabitTracker.exe`.
Put an `app.ico` next to `main.py` to use it as the app icon.

## License

MIT — see [LICENSE](LICENSE).
