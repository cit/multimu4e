[![Build Status](https://travis-ci.org/DamienCassou/multimu4e.svg?branch=master)](https://travis-ci.org/DamienCassou/multimu4e)

# multimu4e

## Summary

Facilitate the configuration of multiple accounts in mu4e

## Installing

You may want to add something like that to your Emacs initialization
file:

```emacs
(require 'multimu4e)
(add-hook 'mu4e-compose-pre-hook #'multimu4e-set-account-in-compose)
(bind-key "C-c F" #'multimu4e-force-account-in-compose)
(setq multimu4e-account-alist
  '(("Account1"
     (multimu4e-account-maildir . "/Account1")
     (mu4e-sent-folder . "/Account1/Saved Items")
     (mu4e-drafts-folder . "/Account1/Drafts")
     (user-mail-address . "my.address@account1.tld")
     (smtpmail-default-smtp-server . "smtp.account1.tld")
     (smtpmail-local-domain . "account1.tld")
     (smtpmail-smtp-user . "username1")
     (smtpmail-smtp-server . "smtp.account1.tld")
     (smtpmail-stream-type . starttls)
     (smtpmail-smtp-service . 25))
    ("Account2"
     (multimu4e-account-maildir . "/Account2")
     (mu4e-sent-folder . "/Account2/Saved Items")
     (mu4e-drafts-folder . "/Account2/Drafts")
     (user-mail-address . "my.address@account2.tld")
     (smtpmail-default-smtp-server . "smtp.account2.tld")
     (smtpmail-local-domain . "account2.tld")
     (smtpmail-smtp-user . "username2")
     (smtpmail-smtp-server . "smtp.account2.tld")
     (smtpmail-stream-type . starttls)
     (smtpmail-smtp-service . 587))))
```

## Contributing

Yes, please do! See [CONTRIBUTING][] for guidelines.

## License

See [COPYING][]. Copyright (c) 2015 Damien Cassou.


[CONTRIBUTING]: ./CONTRIBUTING.md
[COPYING]: ./COPYING
