# Abyss Theme for VS Code

## What This Project Is

Abyss Theme for VS Code is a dark theme built around a pure-black workbench and editor. It keeps the familiar Dark+ syntax palette while removing the gray surfaces that normally remain in tabs, panels, menus, inputs, terminals, notifications, and other VS Code UI areas.

For JetBrains IDEs, use [Abyss Theme for JetBrains](https://github.com/jadchene/abyss-theme-for-jetbrains).

## Why Use It

- Pure-black workbench and editor backgrounds.
- Dark+ syntax highlighting without an unfamiliar language palette.
- Clear white foregrounds and neutral grayscale interaction states.
- Consistent tab, Git decoration, menu, quick-input, terminal, and notification colors.
- Custom Windows title-bar controls that inherit the black title bar.
- Visible neutral-gray text selection in search and other input fields.

## Quick Start

1. Download or build the `.vsix` package.
2. In VS Code, open **Extensions**.
3. Open the Extensions menu and choose **Install from VSIX...**.
4. Select the package and reload VS Code when prompted.
5. Open **Preferences: Color Theme** and select **Abyss Theme for VS Code**.

## Reference

| Item | Value |
| --- | --- |
| Minimum VS Code version | `1.80.0` |
| Extension version | `1.1.9` |
| Extension name | `abyss-theme-for-vscode` |
| Theme picker label | `Abyss Theme for VS Code` |
| Base UI theme | `vs-dark` |
| Syntax highlighting | Dark+ |
| Default window controls | `window.controlsStyle: custom` |
| License | MIT |

The theme definition is in `themes/abyss-color-theme.json`. The bundled `dark_plus.json` and `dark_vs.json` files provide the inherited syntax colors.

## Development

Install the VS Code extension packaging tool:

```powershell
npm install --global @vscode/vsce
```

Validate the JSON files and create a package:

```powershell
Get-Content -Raw package.json | ConvertFrom-Json | Out-Null
Get-Content -Raw themes/abyss-color-theme.json | ConvertFrom-Json | Out-Null
vsce package --no-dependencies
```

The generated `.vsix` can be installed locally through **Install from VSIX...**.

## License

Licensed under the [MIT License](LICENSE).
