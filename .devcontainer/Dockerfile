# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.194.3/containers/ubuntu/.devcontainer/base.Dockerfile

# [Choice] Ubuntu version: hirsute, bionic, focal
ARG VARIANT="hirsute"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-${VARIANT}

# [Optional] Uncomment this section to install additional OS packages.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>

ENV GEM_PATH="/usr/local/rvm/gems/default:/usr/local/rvm/gems/default@global" \
    GEM_HOME="/usr/local/rvm/gems/default" \
    MY_RUBY_HOME="/usr/local/rvm/rubies/default" \
    PATH="/usr/local/rvm/rubies/default/bin:/usr/local/rvm/gems/default@global/bin:/usr/local/rvm/gems/default/bin:/usr/local/rvm/rubies/default/bin:/usr/local/rvm/bin:${PATH}"
COPY library-scripts/ruby-debian.sh /tmp/library-scripts/
RUN apt-get update && bash /tmp/library-scripts/ruby-debian.sh