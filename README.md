# BarsStarter

Monorepo with a SwiftUI starter app and **BarsKit** (Swift Package) providing AppShell + configurable top/bottom bars via `.bars(...)`.

## Structure
- `Packages/BarsKit` — SPM package (`AppShell`, `BarsRouter`, `TitleBar`, `BigBar`)
- `Apps/StarterApp` — minimal SwiftUI app using `BarsKit` (Home, Feature A with scroll-aware bars, About), PL/EN localization

## Quick start (Xcode)
1. Open your iOS app project (or create a new one).
2. **File → Add Packages… → Add Local…** → select `Packages/BarsKit`.
3. Copy `Apps/StarterApp/*` into your project (or use it as your main app).
4. Build & run.

## Usage
```swift
List { /* ... */ }
  .bars(
    top:    [bar { TitleBar(title: "home.title") { Color.clear.background(.thinMaterial) } }],
    bottom: [bar { BigBar(title: "home.cta") { Color.accentColor } }]
  )
