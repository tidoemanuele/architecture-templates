# Common Features Checklist

Project-agnostic features that every new Android app should implement.

---

## Firebase & Analytics
- [ ] Firebase Analytics integration
- [ ] Firebase Crashlytics with privacy opt-in
- [ ] Firebase Remote Config (feature flags)
- [ ] CrashReportingTree for Timber → Crashlytics
- [ ] Analytics opt-in consent flow

## Monetization
- [ ] AdMob SDK setup (publisher ID: `ca-app-pub-8027163152836505`)
- [ ] AdMob banner ads
- [ ] AdMob interstitial ads
- [ ] AdMob rewarded ads
- [ ] AdFrequencyTracker (ad rate limiting)
- [ ] Test ad switching for debug builds
- [ ] Premium flavor ad exclusion (`BuildConfig.IS_PREMIUM`)

## User Engagement
- [ ] In-App Review API prompt
- [ ] Rating dialog timing logic
- [ ] First launch detection
- [ ] Session counting for engagement triggers

## Legal & Compliance
- [ ] Privacy policy (Markdown + viewer screen)
- [ ] Terms of service
- [ ] GDPR analytics/crash opt-in
- [ ] Legal document fragment/screen
- [ ] "Last updated" date in legal docs

## Build Configuration
- [ ] Product flavors: `free` / `premium`
- [ ] `applicationIdSuffix = ".premium"` for premium
- [ ] Signing configs (release keystore)
- [ ] ProGuard/R8 minification
- [ ] Resource shrinking
- [ ] `BuildConfig.IS_PREMIUM` flag

## CI/CD & Automation
- [ ] GitHub Actions: `ci.yml` (lint, test, debug APK)
- [ ] GitHub Actions: `release.yml` (AAB, Play Store deploy)
- [ ] Play Store upload scripts (Python + Google API)
- [ ] Store listing metadata automation
- [ ] Concurrency groups for CI

## Documentation Standards
- [ ] AGENTS.md (AI agent instructions)
- [ ] CLAUDE.md (same or symlink)
- [ ] docs/PRD.md
- [ ] docs/architecture.md
- [ ] .agents/ sub-guides (commands, testing, style)
- [ ] CONTRIBUTING.md
- [ ] CHANGELOG.md

## Play Store Infrastructure
- [ ] playstore/ folder structure (free/premium)
- [ ] Store listing metadata (title, descriptions)
- [ ] Changelog management
- [ ] Screenshot organization
- [ ] Asset specifications doc
- [ ] play-store-upload-release.py script

## Testing Infrastructure
- [ ] JUnit 4
- [ ] MockK / Mockito
- [ ] Turbine (Flow testing)
- [ ] Robolectric
- [ ] kotlinx-coroutines-test
- [ ] HiltTestRunner
- [ ] Room schema exports

## Code Quality
- [ ] Detekt configuration
- [ ] Android Lint baseline
- [ ] EditorConfig
- [ ] ktlint (optional)
- [ ] detekt-config.yml

## Architecture & DI
- [ ] Clean Architecture (3-layer)
- [ ] MVVM pattern
- [ ] Hilt DI
- [ ] AppModule, DatabaseModule, RepositoryModule
- [ ] AdsModule, AnalyticsModule, FirebaseModule

## Common UI Components
- [ ] Splash screen (`core-splashscreen`)
- [ ] Settings screen (theme, privacy, about)
- [ ] Theme management (Light/Dark/System)
- [ ] Legal document viewer
- [ ] Onboarding flow (optional)

## Logging & Debug
- [ ] Timber logging framework
- [ ] LeakCanary (debug only)
- [ ] Debug vs Release tree switching

## Core Dependencies (Version Catalog)
- [ ] Kotlin 2.0+
- [ ] AGP 8.7+
- [ ] Compose BOM
- [ ] AndroidX Core KTX
- [ ] Lifecycle components
- [ ] Room database
- [ ] DataStore preferences
- [ ] WorkManager

## Gradle Configuration
- [ ] gradle.properties standardized
- [ ] Version catalog (libs.versions.toml)
- [ ] JVM 17 target
- [ ] MinSDK 26, TargetSDK 35-36

## Secrets Management
- [ ] secrets/ folder (gitignored)
- [ ] google-services.json per flavor
- [ ] Play Store service account JSON
- [ ] local.properties for dev keys

---

**Last Updated:** January 2026
