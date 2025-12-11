# Ansible Development Environment Setup

Automated setup for development environment including zsh, dotfiles, Docker, Node.js, Go, Rust, and BorderWise repositories.

## Quick Start

1. **Clone this repository:**
   ```bash
   git clone https://github.com/yourusername/ansible.git
   cd ansible
   ```

2. **Install Ansible:**
   ```bash
   sudo apt install software-properties-common
   sudo apt-add-repository --yes --update ppa:ansible/ansible
   sudo apt install ansible
   ```

3. **Run the playbook:**
   ```bash
   ansible-playbook ./local.yml --ask-become-pass
   ```
   Enter your sudo password when prompted.

## What Gets Installed

- **Shell**: Zsh with Oh-My-Zsh and Powerlevel10k theme
- **Dotfiles**: Personal configurations from .dotfiles repository
- **Development Tools**:
  - Node.js (via NVM)
  - Go (latest)
  - Rust (via rustup)
  - Docker with Docker Compose
- **CLI Tools**: fzf, fd-find
- **Repositories**: BorderWise projects (Web, WebWatcher, UserManagement, DevTools)

## Run Specific Tasks

Use tags to run only specific installations:

```bash
ansible-playbook ./local.yml --ask-become-pass --tags "zsh"
ansible-playbook ./local.yml --ask-become-pass --tags "docker"
ansible-playbook ./local.yml --ask-become-pass --tags "go,rust"
ansible-playbook ./local.yml --ask-become-pass --tags "borderwise"
```
