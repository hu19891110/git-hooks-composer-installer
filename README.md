Git Hooks Composer Installer
===========================
[![Latest Stable Version](https://poser.pugx.org/ams/git-hooks-installer/v/stable)](https://packagist.org/packages/ams/git-hooks-installer)
[![Total Downloads](https://poser.pugx.org/ams/git-hooks-installer/downloads)](https://packagist.org/packages/ams/git-hooks-installer)
[![SensioLabsInsight](https://insight.sensiolabs.com/projects/c1015283-d2e4-49b6-8094-b3187873e50e/mini.png)](https://insight.sensiolabs.com/projects/c1015283-d2e4-49b6-8094-b3187873e50e)
[![License](https://poser.pugx.org/ams/git-hooks-installer/license)](https://packagist.org/packages/ams/git-hooks-installer)

This plugin helps you automate the installation git hooks using [composer](https://github.com/composer/composer).

Installation
------------
Just run the following command:

    php composer.phar require --dev ams/git-hooks-installer

or if you prefer add the following to the `composer.json` file:

    {
        "require-dev": {
            "ams/git-hooks-installer": dev-master"
        },
        "extra": {
            "git-root-dir": "."
        }
    }

Usage
-----
When the git-hooks-composer installer is run, it only looks for git-hooks among your project dependencies. If your package
is a git hook and you want it to be installed with composer automatically you'll need to define a `composer.json` as follows:

    {
        "type": "git-hook"
    }
    
<aside class="warning">
The git hooks scripts should be located in the package root directory.
</aside>

Currently are the following git hooks supported:
* `applypatch-msg`
* `pre-applypatch`
* `post-applypatch`
* `pre-commit`
* `prepare-commit-msg`
* `commit-msg`
* `post-commit`
* `pre-rebase`
* `post-checkout`
* `post-merge`
* `pre-push`
* `pre-receive`
* `update`
* `post-receive`
* `post-update`
* `pre-auto-gc`
* `post-rewrite`


Contribute
----------

Contributions to are very welcome!

* Report any bugs or issues you find on the [issue tracker].

Support
-------

If you are having problems, send a mail to contact@amansilla.com or just write me [@flamingek] on Twitter.

License
-------

All contents of this package are licensed under the [MIT license].

[issue tracker]: https://github.com/amansilla/git-hooks-composer-installer/issues
[MIT license]: LICENSE
[@flamingek]: https://twitter.com/flamingek
