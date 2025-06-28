---
comments: true
---
# Шпаргалка по tmux

## Конфигурация tmux
```title=".tmux.conf"
set -g default-terminal "screen-256color"

set -g prefix C-a

bind s choose-tree -sZ -O name

set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'
set -g @plugin 'jimeh/tmux-themepack'
set -g @themepack 'powerline/double/green'


unbind %
bind | split-window -h

unbind '"'
bind - split-window -v
set -g mouse on

# Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
run '~/.tmux/plugins/tpm/tpm'
```

В качестве префикса будет использоваться не `Ctrl + B`, а `Ctrl + A`, что гораздо удобнее. Также заменяем вертикальное и горизонтальное разделение (об этом позднее).