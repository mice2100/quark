# Sciter.js Quark (Updated)

This is an updated version of the Sciter.js Quark application, based on Sciter **v6.0.3.10**.

## ✨ New Features & Improvements

1. **Custom Settings via Command Line**  
   You can now pass a specific settings JSON file via the command line to override the default configuration for the build process.

2. **Direct Assembly (`assemble=0`)**  
   Support for a new command-line argument `assemble=0` (or another project index). Passing this argument automatically initiates the assembly process for the specified project and exits immediately after.

3. **Multiple Entry File Support**  
   The application now checks for multiple possible entry file names when validating a project folder. It looks for:
   - `run.js`
   - `index.htm`
   - `main.htm`
   *(The original version only checked for `main.htm`)*

4. **Standalone Assembly Support**  
   Added a check for an additional quark binary for `scapp`, allowing Quark to be assembled into a fully stand-alone executable by itself - You need to copy packfolder as well to the executable folder. For macos, this is quark.app/Contents/MacOSX/packfolder, for windows, this is quark.exe + packfolder.exe.

## 🐛 Bug Fixes

- **Assemble Button State Fixed**: Addressed a bug where the "Assemble" button was incorrectly remaining disabled upon launching the application, even if a valid project was selected.
