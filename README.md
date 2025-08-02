# Terminal Configuration

This repository contains terminal configurations optimized for development work, featuring a dark theme with transparency effects, consistent color schemes, and fish shell integration.

## Terminal Emulators

### Ghostty Terminal

#### Configuration

The Ghostty configuration is located in `terminal/ghostty.config`.

**Installation & Setup:**

1. **Install Ghostty:**

   ```bash
   # macOS (via Homebrew)
   brew install --cask ghostty
   
   # Or download from https://ghostty.org
   ```

2. **Apply Configuration:**

   ```bash
   # Create config directory if it doesn't exist
   mkdir -p ~/.config/ghostty
   
   # Create symlink to keep configuration in sync
   ln -sf "$(pwd)/terminal/ghostty.config" ~/.config/ghostty/config
   ```

3. **Restart Ghostty** to apply the new configuration.

### iTerm2 Terminal

#### Configuration

The iTerm2 configuration is located in `terminal/iterm2-config.json`.

**Installation & Setup:**

1. **Install iTerm2:**

   ```bash
   # macOS (via Homebrew)
   brew install --cask iterm2
   
   # Or download from https://iterm2.com
   ```

2. **Import Configuration:**

   ```bash
   # Open iTerm2
   # Go to: Preferences > Profiles > Other Actions... > Import JSON Profiles
   # Select: terminal/iterm2-config.json
   ```

3. **Set as Default Profile:**

   ```bash
   # Open iTerm2
   # Go to: Preferences > Profiles, select the imported "Custom Profile"
   # Click "Other Actions..." > "Set as Default"
   ```

4. **Install Font (if needed):**

   ```bash
   # Install JetBrains Mono Nerd Font
   brew install font-jetbrains-mono-nerd-font
   ```

## Fish Shell Configuration

Both terminal configurations use Fish shell with custom configurations.

### Fish Setup

```bash
# Install Fish shell
brew install fish

# Set Fish as default shell
echo /opt/homebrew/bin/fish | sudo tee -a /etc/shells
chsh -s /opt/homebrew/bin/fish

# Apply Fish configuration (create symlinks to keep in sync)
mkdir -p ~/.config/fish
ln -sf "$(pwd)/fish/config.fish" ~/.config/fish/config.fish
ln -sf "$(pwd)/fish/fish_variables" ~/.config/fish/fish_variables
```

## Starship Prompt

The configuration includes Starship prompt customization.

### Starship Setup

```bash
# Install Starship
brew install starship

# Apply configuration (create symlink to keep in sync)
mkdir -p ~/.config
ln -sf "$(pwd)/starship/starship.toml" ~/.config/starship.toml
```
