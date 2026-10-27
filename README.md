# Wpress Extractor

A small Go-based utility for extracting WordPress migration archives with the `.wpress` extension. This repository contains a Go source tree and prebuilt binaries for some platforms.

## Purpose

The tool is intended to unpack a `.wpress` archive created by the All-in-One WP Migration WordPress plugin into files that can be inspected or restored manually.

## Technology

- Go
- Command-line file/archive handling
- Windows/macOS binaries are included in the repository

## Usage

Download or build the executable appropriate for your operating system, then pass the archive path as the first command-line argument:

```bash
./wpress-extractor /path/to/backup.wpress
```

On Windows, run the executable from Command Prompt or PowerShell and pass the full path to the archive. Use a separate output directory and keep an untouched backup of the original file.

## Build from source

Install a Go toolchain compatible with the source, clone the repository, and inspect the module/source layout before building. The prebuilt `dist/` files may not be reproducible from the checked-in source without verifying the original build instructions.

## Credits and licensing

This repository acknowledges the original implementation at [yani-/wpress](https://github.com/yani-/wpress); the original README describes a small modification to support Windows execution. Review the upstream project's license and preserve required attribution when distributing derived code or binaries.

## Safety

Only extract archives you are authorized to access. Treat the extracted WordPress files as potentially sensitive; backups can contain credentials, user data, plugins, and configuration files. Do not upload private backups to public repositories.
