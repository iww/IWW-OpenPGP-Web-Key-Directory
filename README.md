# OpenPGP Web Key Directory for [iww.org](https://iww.org)

On system with @iww.org keys, in directory **.well-known**, run:

```sh
gpg --list-options show-only-fpr-mbox -k "@iww.org" | $(gpgconf --list-dirs libexecdir)/gpg-wks-client -v --install-key
```

*Requires **GPG >= 2.2.12** with **gpg-wks-client** (on macOS, must compile from [source](https://gnupg.org/download/index.html)).*

To test WKD, run:

```sh
gpg --auto-key-locate clear,wkd,nodefault --verbose --locate-key example@iww.org
```

References:
- https://wiki.gnupg.org/WKDHosting
- https://tools.ietf.org/id/draft-koch-openpgp-webkey-service-05.html
- https://github.com/mihalyr/openpgpkey
