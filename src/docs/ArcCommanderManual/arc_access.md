---
layout: docs
title: ARC Commander DataHUB access
date: 2023-11-23
author:
- name: Martin Kuhl
  github: https://github.com/Martin-Kuhl
  orcid: https://orcid.org/0000-0002-8493-1077
- name: Dominik Brilhaus
  github: https://github.com/brilator
  orcid: https://orcid.org/0000-0001-9021-3197
add toc: true
add support: false
add sidebar: _sidebars/mainSidebar.md
---

The [DataHUB](<https://git.nfdi4plants.org>) allows you to share your ARCs with registered lab or project partners. After [registration](<https://register.nfdi4plants.org>), you need to setup the ARC Commander for smooth ARC synchronization between your computer and the DataHUB.

:bulb: This needs to be done only once per computer.

## Enable Git to store credentials on your computer

Open a command prompt or terminal and execute the following command(s)

### Windows

```bash
git config --global credential.helper cache
```

and / or  

```bash
git config --global credential.helper store
```

### MacOS

```bash
git config --global credential.helper osxkeychain
```

### Linux

```bash
git config --global credential.helper store
```

## Receive and store a DataHUB access token

```bash
arc remote accesstoken get -s https://git.nfdi4plants.org
```

A browser window will open asking for your DataPLANT login. After login you are asked to authorize your computer to communicate with the DataHUB.  
In case you are already logged in, the browser will directly display a plain `Success` message to you.

:bulb: This authenticates your computer to communicate with your personal DataHUB account
