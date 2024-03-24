# Laravel Pint Pre-Commit Hook

This script runs [Laravel Pint](https://laravel.com/docs/master/pint) before committing your code.

Laravel Pint is **run quietly** to avoid any output which is ideal for CI pipelines.

Only **changed/dirty files** since the last commit are checked.

This hook is invoked by `git commit`, and [can be bypassed](https://git-scm.com/docs/githooks#_pre_commit) using the `--no-verify` option.

```sh
git commit --no-verify
```

## Installation

Create the hooks directory:

```sh
mkdir ~/.githooks
```

Download or copy the `pre-commit` script to:

```sh
~/.githooks/pre-commit
```

Ensure the file is executable:

```sh
chmod 744 ~/.githooks/pre-commit
```

Configure the Git [hooks path](https://git-scm.com/docs/git-config#Documentation/git-config.txt-corehooksPath):

```sh
git config --global core.hooksPath ~/.githooks
```

## Using PHP_CS_Fixer?

This work was heavily inspired by [PHP-CS-Fixer Pre-Commit Hook](https://github.com/gerardroche/php-cs-fixer-pre-commit-hook) and it is an excellent alternative for those using PHP_CS_Fixer.

## License

Released under the [GPL-3.0-or-later License](LICENSE).