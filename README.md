# Github — Mobile

## Template copy

This repo is one of the name-substituted Flutter template copies in
`bookchaowalit-mobile`. The canonical Flutter template is
[`bookchaowalit-mobile/education-coursenotes-mobile`](https://github.com/bookchaowalit-mobile/education-coursenotes-mobile);
fixes land there first and are copied here (this repo owns its copy, no shared
package). Consolidation or archiving is pending owner decision D5 (BD-033), see
`repository-catalog/portfolio/MOBILE-CONSOLIDATION-2026-10.md` in solo-empire.

Bare Flutter scaffold for a **Github** mobile app: three placeholder tabs
(Home, Explore, Profile) and no app logic, data or network access yet.

Part of [Chaowalit Greepoke](https://bookchaowalit.com)'s 101 Portfolio Projects.

## Tech Stack

- **Framework:** Flutter (CI pinned to 3.47.5) + Material 3
- **Language:** Dart
- **State / navigation:** `setState` and a bottom `NavigationBar`.
  `flutter_riverpod` and `go_router` are declared in `pubspec.yaml` but not
  used by any code yet.

## Getting Started

```bash
flutter pub get
flutter run
```

## Verify

```bash
flutter pub get --enforce-lockfile
dart format --output=none --set-exit-if-changed lib
flutter analyze
flutter build apk --debug
```

CI (`.github/workflows/build.yml`) pins Flutter in the workflow `env` and runs
exactly these steps, all fail closed, plus the shared `platform-ci-workflows`
`security.yml` scan. There are no tests yet because there is no logic to test.

## Build

```bash
# Android (debug)
flutter build apk --debug
```

Release builds are currently signed with the Android debug key (Flutter
template default), so they are not store builds. There is no `ios/` project in
this repo.

## Related

- **Frontend:** [bookchaowalit-website/github-frontend](https://github.com/bookchaowalit-website/github-frontend)
- **Portfolio:** [bookchaowalit.com](https://bookchaowalit.com)

## License

MIT
