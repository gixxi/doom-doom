# doom-doom
Doom Emacs's user configuration directory

The ~/.config/doom/ directory is Doom Emacs's user configuration directory — it's where you customize Doom to your liking, separate from Doom's own source code (which lives in ~/.config/emacs/ or ~/.emacs.d/).
It typically contains three key files:
init.el — Controls which Doom modules are enabled. It's essentially a list of (doom! ...) declarations where you toggle features like lsp, magit, org, vterm, language support, etc. Think of it as your feature manifest.
config.el — Your main personal configuration. This is where you set keybindings, theme, font, package settings, hooks, and any custom Elisp. It's loaded after Doom's own defaults, so your settings override theirs.
packages.el — Declares additional packages (beyond what Doom modules provide). You use (package! ...) forms here to pull packages from MELPA, GitHub, etc.
After editing any of these, you run doom sync from the terminal to reconcile your declarations with the actual installed state — it installs/removes packages, rebuilds autoloads, and byte-compiles as needed.
You might also see a custom.el in there if Emacs's customize system has written anything, though Doom generally discourages using the customize UI in favor of explicit Elisp in config.el.
