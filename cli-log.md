# CLI Command Logger

A terse CLI command logging for system configuration tasks.

## Instructions

When performing system setup, installation, or configuration tasks (OpenSSH, Docker, nginx, etc.), log the actual steps performed in a concise format suitable for developer notes.

### Format Requirements

- Maximum ~20 lines for complete procedure
- One line per logical step
- Use actual commands executed (not descriptions)
- Omit verbose output, confirmations, or explanations
- Include only critical configuration changes
- Format: command or brief action statement

### Example Format

```
sudo apt update
sudo apt install -y openssh-server
sudo nano /etc/ssh/sshd_config → PermitRootLogin no, PasswordAuthentication yes
sudo systemctl enable ssh
sudo systemctl start ssh
sudo ufw allow 22/tcp
sudo systemctl status ssh → verified running
```

### What to Include

- Package manager commands (apt, yum, dnf, etc.)
- Service management (systemctl, service)
- Key configuration file edits (show file path + specific changes with →)
- Firewall rules if applicable
- Verification steps (status checks, tests)

### What to Omit

- Command output (unless critical error)
- Explanatory text
- Warning messages
- Package download progress
- Routine confirmations

### Output Location

Present the log as a code block at the END of the task, after all steps are complete.
