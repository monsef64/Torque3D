# Torque3D (Wayland Fork)

This is [monsef64/Torque3D](https://github.com/monsef64/Torque3D) — a fork of the MIT licensed open source [Torque3D](https://torque3d.org) engine from [GarageGames](http://www.garagegames.com), maintained upstream by [TorqueGameEngines](https://github.com/TorqueGameEngines/Torque3D).

**What's different in this fork:** native X11 support has been removed from the Linux build and replaced with native **Wayland** support. Linux windowing, input, and font/DPI handling now go through SDL2's Wayland backend and FreeType/Fontconfig instead of X11-specific code paths. See the [branch history](https://github.com/monsef64/Torque3D/commits/arena/ffc320cb-torque3d) for the relevant changes.

[![GitHub tag](https://img.shields.io/github/tag/monsef64/Torque3D.svg)](https://github.com/monsef64/Torque3D/tags)
[![GitHub release](https://img.shields.io/github/release/monsef64/Torque3D.svg)](https://github.com/monsef64/Torque3D/releases/latest)
[![Github All Releases](https://img.shields.io/github/downloads/monsef64/Torque3D/total.svg)](https://github.com/monsef64/Torque3D/releases/latest)

[![Discord](https://img.shields.io/badge/Discord%20-%237289DA.svg?&logo=discord&logoColor=white)](https://discord.com/invite/qdAZxT4)
[![IRC](https://img.shields.io/badge/irc-%23garagegames-green.svg)](https://kiwiirc.com/client/irc.maxgaming.net/?nick=wiki_user|?#garagegames)

**Build Status (upstream):**

[![Windows Build](https://github.com/TorqueGameEngines/Torque3D/actions/workflows/build-windows-msvc.yml/badge.svg)](https://github.com/TorqueGameEngines/Torque3D/actions/workflows/build-windows-msvc.yml)

[![Linux Build](https://github.com/TorqueGameEngines/Torque3D/actions/workflows/build-linux-gcc.yml/badge.svg)](https://github.com/TorqueGameEngines/Torque3D/actions/workflows/build-linux-gcc.yml)

[![MacOSX Build](https://github.com/TorqueGameEngines/Torque3D/actions/workflows/build-macos-clang.yml/badge.svg)](https://github.com/TorqueGameEngines/Torque3D/actions/workflows/build-macos-clang.yml)

## Releases

Pre-built Linux x86_64 binaries for this fork are published on the [GitHub Releases page](https://github.com/monsef64/Torque3D/releases). Each release is built with CMake + Ninja (RelWithDebInfo) against SDL2's Wayland backend, with no X11 dependency.

## Wayland Migration Notes

* X11-specific window/input/font code paths have been removed from the Linux engine build.
* `Engine/source/platformWayland/` contains the new Wayland-oriented font handling (via FreeType/Fontconfig) that replaces the old X11 font lookup code.
* `windowManager/sdl/sdlWindow.cpp` and related CMake wiring now prefer SDL's `SDL_WAYLAND` video driver and disable `SDL_X11` on Linux builds.
* The engine still builds and links cleanly with gcc/CMake/Ninja on Linux with these changes in place — see the Releases page for a working compiled build.

## More Information

* [Homepage](https://torque3d.org)
* [Torque 3D wiki](http://wiki.torque3d.org)
* [Community forum](https://torque3d.org/forums)
* [Roadmap](https://github.com/orgs/TorqueGameEngines/projects/1)
* [Upstream Binaries](https://github.com/TorqueGameEngines/Torque3D-Binaries)
* [Guide Docs](https://docs.torque3d.org/)
* [Reference Docs](https://reference.torque3d.org/)
* [Work Blog](https://torque3d.org/blogs/blog/1-work-blog/)

**Extras:**
[Torque3D Resources](https://github.com/Torque3DResources) | [Awesome Torque3D](https://github.com/TorqueGameEngines/awesome-torque3d)

## Pre-compiled Version

* This fork's Linux builds (Wayland, no X11): [monsef64/Torque3D Releases](https://github.com/monsef64/Torque3D/releases)
* Upstream pre-packaged files for Windows/macOS/Linux: [Torque3D Binaries](https://github.com/TorqueGameEngines/Torque3D-Binaries)

### Legacy Links
* [Legacy Repository](https://github.com/GarageGames/Torque3D)
* [GarageGames forum](http://www.garagegames.com/community/forums)
* [GarageGames professional services](http://services.garagegames.com/)
* [Project Manager repository](https://github.com/GarageGames/Torque3D-ProjectManager)
* [Offline documentation repository](https://github.com/Torque3D-GameEngine/Torque3D-Documentation)

### Upstream Repository
* [TorqueGameEngines/Torque3D](https://github.com/TorqueGameEngines/Torque3D) — the original upstream project this fork tracks.

# License

All assets and code are under the [![license](https://img.shields.io/github/license/GarageGames/Torque3D.svg)](https://github.com/GarageGames/Torque3D/blob/master/LICENSE.md)
