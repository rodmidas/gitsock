# gitsock

> Easily use different git accounts for different projects

This is a CLI tool to create and store multiple git identities & apply them to repositories.

Example:

```sh
gitsock mk steve steve@apple.com "Steve Gates"
cd path/to/repo
gitsock use steve
git commit ...
```

You can also force yourself to use gitsock and prevent accidents by removing the global identity:

```sh
git config --global --unset user.name
git config --global --unset user.email
```

```
Usage:
  gitsock ls                         List socks
  gitsock mk <sock> <email> <name>   Create a new sock
  gitsock rm <sock>                  Remove a sock
  gitsock status                     Show current repo's sock
  gitsock key <sock>                 Display a sock's public key
  gitsock use <sock>                 Use a sock for current repo
```