---
layout:     post
title:      Configuring git credential cache on linux
date:       2018-06-09 12:32:18
summary:    Use git without set yours credentials all time you push or pull, set git credential cache for password free.
categories: jekyll pixyll
---

# Configuring git-credential-cache on linux

The git-credential-cache is a useful tool to remember your HTTP/HTTPS git credentials (though you really should be using SSH instead). It’s useful for things like long passwords or access tokens. It stores them in memory for a certain number of seconds.

### Enabling it
$ git config --global credential.helper cache

### Setting the timeout
- Set the time to rember your credentials for (in seconds). The command below sets it to 10 minutes.
$ git config --global credential.helper 'cache --timeout=600'

### Disabling it
$ git config --global --unset credential.helper
