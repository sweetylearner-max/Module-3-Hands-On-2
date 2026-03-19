# App with Implicit Intents

An Android app that demonstrates implicit intents to interact with other apps — opening a browser, sending email, sharing text, dialing a phone, and opening maps.

---

## Output Screenshots

<p align="center">
  <img src="https://github.com/user-attachments/assets/c4bb5b17-168d-4db8-9ac5-3d0f74bb8264" width="22%"/>
  <img src="https://github.com/user-attachments/assets/727ba827-3e95-4ab7-9657-eabb4e7624fa" width="22%"/>
  <img src="https://github.com/user-attachments/assets/36766ed1-2bdf-4987-a488-bfb94fb3a3a7" width="22%"/>
  <img src="https://github.com/user-attachments/assets/e23012cb-5b3e-4955-a3f3-2b4e1666213a" width="22%"/>
</p>

## Features

| Action | Intent Used |
|--------|------------|
| Open Web Page | `ACTION_VIEW` with `Uri.parse(url)` |
| Send Email | `ACTION_SENDTO` with `mailto:` URI + extras |
| Share Text | `ACTION_SEND` with `text/plain` + `createChooser()` |
| Dial Phone | `ACTION_DIAL` with `tel:` URI |
| Open Maps | `ACTION_VIEW` with `geo:` URI |

---

## Project Structure

```
src/main/
├── java/com/project/mod3pro2/
│   └── MainActivity.kt       ← All implicit intent actions
└── res/
    ├── layout/activity_main.xml  ← ScrollView with 5 sections
    └── values/strings.xml        ← All labels and hints
```

---

## How It Works

1. User enters input (URL / email / text) in EditText fields.
2. On button click, an implicit Intent is created with the appropriate action and data.
3. Android resolves the Intent to an installed app and launches it.
4. If no app handles the Intent, a Toast is shown.

---

## Requirements

- Android Studio Hedgehog or later
- Min SDK: 24
- Language: Kotlin
- Theme: Material Components Purple (`#FF6200EE`)
