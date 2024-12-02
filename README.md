# DownmarkerWPF

[![Build status](https://ci.appveyor.com/api/projects/status/8nyixeikl67jh305/branch/master?svg=true)](https://ci.appveyor.com/project/shiftkey/downmarkerwpf/branch/master)

This codebase contains the [DownmarkerWPF](http://code52.org/DownmarkerWPF/) project, by [Code52](http://code52.org/)

## About DownmarkerWPF

MarkPad (formerly known as DownmarkerWPF) is an editor for [Markdown](http://daringfireball.net/projects/markdown/) - a widely used syntax for formatting plain text to convert to blogs, comments, and in other places like on [Stack Overflow](http://stackoverflow.com/).

Our aim is to create a useably, stylish new version of the project utilising Microsoft's WPF technology to provide a fresh UI for creating files that we can use to create blog posts for this, and other blogs using Markdown.

## Install
[Nightly](http://ginnivan.blob.core.windows.net/markpadnightly/MarkPad.application) | [Stable](http://ginnivan.blob.core.windows.net/markpadrelease/MarkPad.application)

Updates will be installed directly through MarkPad.

## Dependencies

 - Windows 7 (please provide feedback if you encounter issues with Vista, XP or Windows 8)
 - .NET Framework 4.0 (should install if you don't already have it on your machine)

## Tools required to develop

 - [Visual Studio](https://www.visualstudio.com/)
 - [WiX](http://wixtoolset.org/releases/v3.9/stable) - to generate the installer (optional)
 - [7-Zip](http://www.7-zip.org/download.html) - to generate a zip version of the tool (optional)

# Recent Contributions: Extended Test Coverage
To ensure the reliability and robustness of the project, I contributed additional unit tests covering various edge cases and functionalities. Below is an overview of my contributions:

## Highlights of the Added Tests:
1. FileMarkdownDocumentTests:

- Added tests to handle unsupported file types, ensuring the application throws an appropriate exception.
- Prevented overwriting files when the content is empty during a save operation.

2. FileSystemSiteItemTests:

- Ensured FileRenamedEvent is ignored when the event references unrelated files.
- Prevented duplicate children from being added to the Children collection when a file creation event occurs.

3. JekyllSiteContextTests:

- Verified that renaming a directory triggers the correct FileRenamedEvent.
- Ensured application stability by handling errors gracefully during file system watcher events.
- These additions aim to improve the overall code quality, catch edge cases, and provide better guarantees for the behavior of the system in various scenarios.