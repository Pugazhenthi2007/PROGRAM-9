#!/bin/bash

# Ensure script exits immediately if a command fails
set -e

# Requirement 1 — Open TCP Port 8080
firewall-cmd --add-port=8080/tcp

# Requirement 2 — Open TCP Port 9000
firewall-cmd --add-port=9000/tcp

# Requirement 3 — List currently configured ports
firewall-cmd --list-ports

# Requirement 4 — Remove TCP Port 8080
firewall-cmd --remove-port=8080/tcp

# Requirement 5 — Permanently open TCP Port 3000
firewall-cmd --add-port=3000/tcp --permanent

# Requirement 6 — Reload the firewall configuration
firewall-cmd --reload

exit 0
