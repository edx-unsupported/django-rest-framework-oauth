<div class="badges">
    <a href="http://travis-ci.org/jpadilla/django-rest-framework-oauth?branch=master">
        <img src="https://secure.travis-ci.org/jpadilla/django-rest-framework-oauth.png?branch=master">
    </a>
    <a href="https://pypi.python.org/pypi/djangorestframework-oauth">
        <img src="https://img.shields.io/pypi/v/djangorestframework-oauth.svg">
    </a>
</div>

---

# REST Framework OAuth

OAuth support for Django REST Framework

---

## Overview

OAuth support extracted as a third party package directly from the official Django REST Framework implementation. It's built to use the [django-oauth-plus][django-oauth-plus], [oauth2][oauth2], and [django-oauth2-provider][django-oauth2-provider] packages.

This package provides two authentication classes, [OAuthAuthentication][oauth-authentication] and [OAuth2Authentication][oauth2-authentication], and a [TokenHasReadWriteScope][token-has-read-write-scope] permission class.

## Requirements

* Python 2.7
* Django (1.6, 1.7)
* Django REST Framework (2.4.3, 2.4.4, 3.0-beta)

## Installation

Install using `pip`:

```bash
$ pip install djangorestframework-oauth
```

OAuth packages are optional and not installed out of the box. Use of `OAuthAuthentication` requires installation of the `django-oauth-plus` and `oauth2` packages:

```bash
$ pip install django-oauth-plus oauth2
```

Use of `OAuth2Authentication` requires installation of `django-oauth2-provider`:

```bash
$ pip install django-oauth2-provider
```

Use of `TokenHasReadWriteScope` requires installation of either `django-oauth-plus` or `django-oauth2-provider`.

## Documentation & Support

Full documentation for the project is available at http://jpadilla.github.io/django-rest-framework-oauth/.

You may also want to follow the [author][jpadilla] on Twitter.

## Testing

Install testing requirements.

```bash
$ pip install -r requirements.txt
```

Run with runtests.

```bash
$ ./runtests.py
```

You can also use the excellent [tox](http://tox.readthedocs.org/en/latest/) testing tool to run the tests against all supported versions of Python and Django. Install tox globally, and then simply run:

```bash
$ tox
```

## Documentation

To build the documentation, you'll need to install `mkdocs`.

```bash
$ pip install mkdocs
```

To preview the documentation:

```bash
$ mkdocs serve
Running at: http://127.0.0.1:8000/
```

To build the documentation:

```bash
$ mkdocs build
```

[oauth-authentication]: authentication.md#oauthauthentication
[oauth2-authentication]: authentication.md#oauth2authentication
[token-has-read-write-scope]: permissions.md#tokenhasreadwritescope
[django-oauth-plus]: http://code.larlet.fr/django-oauth-plus/wiki/Home
[oauth2]: https://github.com/joestump/python-oauth2
[django-oauth2-provider]: http://django-oauth2-provider.readthedocs.org/
[jpadilla]: https://twitter.com/jpadilla_
