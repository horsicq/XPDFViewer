[![GitHub tag (latest SemVer)](https://img.shields.io/github/tag/horsicq/XPDFViewer.svg)](https://github.com/horsicq/XPDFViewer/releases)
[![GitHub All Releases](https://img.shields.io/github/downloads/horsicq/XPDFViewer/total.svg)](https://github.com/horsicq/XPDFViewer/releases)

PDF viewer. It renders the visual content of PDF documents using a self-contained,
first-party PDF engine (no external PDF library). The program works on macOS,
Linux and Windows.

Features:

* Continuous page scrolling with lazy, threaded, cached rendering
* Zoom (fit width / fit page / custom) and cursor-anchored Ctrl+wheel zoom
* Page navigation, rotation, mouse panning, HiDPI-aware output
* Password-protected PDF support
* Drag & drop and recent-files list

The viewer UI is provided by the reusable `pdf_widget` component
(`_mylibs/pdf_widget`), which embeds a first-party PDF parser and renderer
(`_mylibs/pdf_widget/engine`) built on Qt's raster/font/image facilities.

* Download: https://github.com/horsicq/XPDFViewer/releases
* Changelog: https://github.com/horsicq/XPDFViewer/blob/master/changelog.txt

## Building

```
cmake -S . -B build -G "Visual Studio 17 2022" -A x64 -DCMAKE_PREFIX_PATH=C:/Qt/5.15.2/msvc2019_64
cmake --build build --config Release
```

The executable is produced at `build/src/gui/Release/xpdfviewer.exe`. It has no
external PDF-library dependency — only Qt.
