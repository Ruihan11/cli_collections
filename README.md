# cli_collections
This is a linux cli tools collection, just in case i forget.

## Installation (No sudo required)

```bash
# ripgrep (rg): Faster grep
curl -LO https://github.com/BurntSushi/ripgrep/releases/download/14.1.1/ripgrep-14.1.1-x86_64-unknown-linux-musl.tar.gz && tar -xzf ripgrep-14.1.1-x86_64-unknown-linux-musl.tar.gz && mkdir -p ~/.local/bin && mv ripgrep-14.1.1-x86_64-unknown-linux-musl/rg ~/.local/bin/ && rm -rf ripgrep-14.1.1*

# delta: Syntax-highlighted git diff
curl -LO https://github.com/dandavison/delta/releases/download/0.18.2/git-delta_0.18.2_amd64.deb && dpkg-deb -x git-delta_0.18.2_amd64.deb delta-tmp && mkdir -p ~/.local/bin && mv delta-tmp/usr/bin/delta ~/.local/bin/ && rm -rf delta-tmp git-delta*.deb
git config --global core.pager delta
git config --global interactive.diffFilter 'delta --color-only'
git config --global delta.navigate true
git config --global delta.dark true
git config --global merge.conflictStyle zdiff3
git config --global delta.features decorations
git config --global delta.line-numbers true
git config --global delta.syntax-theme Dracula

# dust: Intuitive disk usage analyzer
curl -LO https://github.com/bootandy/dust/releases/download/v1.2.4/dust-v1.2.4-x86_64-unknown-linux-musl.tar.gz && tar -xzf dust-v1.2.4-x86_64-unknown-linux-musl.tar.gz && mkdir -p ~/.local/bin && mv dust-v1.2.4-x86_64-unknown-linux-musl/dust ~/.local/bin/ && rm -rf dust-v1.2.4*

# eza: Modern ls replacement with icons and git status
curl -LO https://github.com/eza-community/eza/releases/download/v0.23.5/eza_x86_64-unknown-linux-gnu.tar.gz && tar -xzf eza_x86_64-unknown-linux-gnu.tar.gz && mkdir -p ~/.local/bin && mv bin/eza ~/.local/bin/ && rm -rf bin eza_x86_64*.tar.gz
```

## Quick Usage

| Tool | Command | Description |
|------|---------|-------------|
| **rg** | `rg -l "pattern" /path` | Search files containing pattern |
| **delta** | `git diff` | Auto-enabled for git diffs |
| **dust** | `dust -d 2 /path` | Show disk usage by folder |
| **eza** | `eza -l --icons --git` | List files with icons & git status |
