# homebrew-linkpilot

Homebrew tap for [LinkPilot](https://github.com/jackerjay/LinkPilot) — a
per-link router that dispatches every URL to the right browser, profile,
and workspace on macOS.

The recipe sources of truth live in the main repo under
`packaging/homebrew/`; this tap is a publish mirror.

## Install

```sh
brew tap jackerjay/linkpilot

# GUI app (.app → /Applications). The build is unsigned, so the cask's
# postflight strips the quarantine flag for you; Homebrew shows a one-time
# tap-trust prompt the first time because postflight runs a shell command.
brew install --cask jackerjay/linkpilot/linkpilot

# CLI only (lpt + linkpilot-daemon on your PATH).
brew install jackerjay/linkpilot/linkpilot-cli
```

LinkPilot ships unsigned (no Apple Developer ID / notarization yet). The
cask de-quarantines the app on install; the formula path doesn't quarantine
downloads at all.
