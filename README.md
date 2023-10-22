# Ansible role: MULTIPLEXER

Setup Tmux and Screen.

Only tested on Archlinux.

## Usage
Override [defaults](https://github.com/lunics/ansible_role_multiplexer/blob/main/defaults/main.yml)
```yaml
tmux: true                  # enable the tmux installation
default_user: foo           # set the target user

binds_multiplexer:          # set the tmux bindings
  leader_key: C-a
  window:
    prev:    M-h
    last:    M-k
    next:    M-l
    search:  M-m
    new:     M-n
    rename:  M-a
    split:
      vert:  "-"
      hori:  "|"
    swap:
      left:  M-Left
      right: M-Right
  pane:
    focus:
      left:  M-S-h
      down:  M-S-j
      up:    M-S-k
      right: M-S-l
    resize:
      down:  M-C-j
      up:    M-C-k
      left:  M-C-h
      right: M-C-l
    swap:
      vert:  M-j
      hori:  M-S-y
  session:
    new:     M-S-z
    search:  M-S-m
  detach:    M-d
  restore:   M-r
```

TODO
- combine a custom and default binds
- add or remove tmux commentaries
- template the tmux plugins into a dict
