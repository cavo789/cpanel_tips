# cPanel

Tips and tricks for cPanel

## Spam

### Get Black/white listed addresses

> [https://forums.cpanel.net/threads/import-and-export-spamassassin-entries.612223/](https://forums.cpanel.net/threads/import-and-export-spamassassin-entries.612223/)

Using your FTP client, go to your user's home directory and you'll find the file `user_prefs` in the `.spamassassin` folder.

That file looks like this:

```text
blacklist_from *@*.hr
blacklist_from *@*.rest
blacklist_from *@*.ru
blacklist_from *@*.su
whitelist_from *@avonture.be
```

Just put your rules in it and save the file.

You can manipulate entries one by one using the web interface too. Go to your cPanel, search for `Spam Filters` and click on `Additional Configurations (For Advanced Users)`.

![Spam filters](./images/spam_filters.png)

You can now manipulate the list with f.i. vscode and sort it alphabetically, simplify rules, remove duplicated entries (after refactoring), ...
