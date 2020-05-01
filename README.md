# [telega](https://github.com/zevlg/telega.el) in a snap #

-------------------------------------------------------------------------------

[![telega](https://snapcraft.io/telega/badge.svg)](https://snapcraft.io/telega)

## Installation ##

[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/telega)

``` shell
sudo snap install telega
```

([Don't have snapd installed?](https://snapcraft.io/docs/core/install))

## Configuration ##

Create an alias for the `telega-server` binary (until this is provided
automatically by the store):

```shell
sudo snap alias telega.telega-server telega-server
```

### `use-package`

We recommend to use [use-package](https://github.com/jwiegley/use-package)

```emacs-lisp
(use-package telega
  :load-path "/snap/telega/current/share/emacs/site-lisp/telega/"
  ;; telega requires visual-fill-column
  :init (use-package visual-fill-column
          :ensure t)
  ;; usual configuration here...
  )
```

### Manual

Telega requires `visual-fill-column` to also be installed.

```emacs-lisp
(add-to-list 'load-path "/snap/telega/current/share/emacs/site-lisp/telega/")
(require 'telega)
;; usual configuration here...
```
