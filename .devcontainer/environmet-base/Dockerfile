# .devcontainer/Dockerfile

# Use the latest official Alpine image as the base
FROM alpine:3.21.3

# Install essential packages:
# ca-certificates: For HTTPS connections (wget, curl, git)
# bash: A more user-friendly shell than ash (default)
# git: For version control
# build-base: Equivalent to build-essential (gcc, make, etc.) - good practice
# wget, curl, unzip, tar: Common utilities for downloading/extracting
# lua5.4: Lua interpreter (check available version if needed, e.g., 'apk search lua')
# neovim: Neovim editor
# lua-language-server: The LSP (often in the 'community' repo, usually enabled by default)
RUn apk update && apk add --no-cache \
    ca-certificates \
    bash \
    git \
    build-base \
    wget \
    curl \
    tree \
    unzip \
    stow \
    tar \
    lua5.4 \
    neovim \
    neovim-doc \
    lua-language-server \
 && rm -rf /var/cache/apk/*

# Optional: Set bash as the default command for new terminals started within the container.
# Alternatively, this can be set in devcontainer.json settings.
# ENV SHELL=/bin/bash

# --- (Optional) Copy project-specific Neovim config ---
# If you have a .nvim directory in your project root containing your config,
# uncomment the following lines to copy it into the container for the root user.
# COPY .nvim /root/.config/nvim

# Note: This setup runs commands as the root user inside the container.
# For better security practices in non-experimental setups, create a non-root user.
