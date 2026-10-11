# OrynLauncher — Official Source

<p align="center">
  <strong>OrynLauncher</strong><br>
  <em>Minecraft: Java Edition on Android</em>
</p>

OrynLauncher is the official source repository for the OrynLauncher Android project. This repository contains the Android launcher, its Gradle build, native integrations, and supporting modules.

> **Project status:** OrynLauncher is actively being developed. Features and builds may change, and a successful build is not guaranteed until the CI workflow finishes successfully.

## Project goals

- Establish OrynLauncher as its own maintained project and identity.
- Improve reliability of Android builds and Java runtime packaging.
- Develop launcher-owned features and a consistent OrynLauncher experience.
- Keep third-party notices, license obligations, and upstream attribution intact.

## Build

### Requirements

- Android SDK and NDK versions compatible with the Gradle project.
- A compatible JDK/Gradle environment.
- Required Java runtime and native build artifacts used by the workflow.

### Build a debug APK

From the repository root:

```bash
chmod +x gradlew
./gradlew :app_pojavlauncher:assembleDebug
```

On Windows, run `gradlew.bat :app_pojavlauncher:assembleDebug`.

If the build fails, check the complete Gradle output and the **Actions** tab for the failing step. A successful dependency-download step does not mean the APK build succeeded.

## Repository layout

- `app_pojavlauncher/` — Android application module. The module/package names are retained for compatibility with the existing codebase while the project is being migrated.
- `jre_lwjgl3glfw/` — GLFW/JRE integration module.
- `arc_dns_injector/` — DNS support module.
- `forge_installer/` — Forge installer support.
- `.github/workflows/` — automated build workflows.

## Project identity and migration notes

The repository and user-facing project identity are OrynLauncher. Some internal module names, Java package names, dependencies, and legacy implementation details still reflect the upstream foundation. They are intentionally not bulk-renamed until imports, Android authorities, native build scripts, and runtime paths can be migrated safely.

OrynLauncher is **not yet a fully independent implementation** of every launcher subsystem. The project will separate and replace components incrementally, with build and runtime validation at each step.

## Licensing and third-party credits

This project contains code and components derived from or distributed with upstream open-source projects, including PojavLauncher and its dependencies. Their existing copyright notices, license files, and attribution requirements must be preserved. OrynLauncher branding does not change the licenses of those components.

See [LICENSE](LICENSE) and the relevant third-party notices before redistributing modified builds.

## Contributing

Please report reproducible bugs with:
- Device model and Android version
- OrynLauncher version/commit
- Minecraft version and renderer/runtime configuration
- Full relevant error log or failed GitHub Actions step

## Official repository

[OrynLauncher-Official/OrynLauncher-Zero](https://github.com/Orynlauncher-Official/OrynLauncher-Zero)
