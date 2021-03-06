pytest-postgres: pytest support for PostgreSQL in Docker container
============

[![Build Status](https://travis-ci.org/clayman74/pytest-postgres.svg?branch=master)](https://travis-ci.org/clayman74/pytest-postgres)
[![Coverage Status](https://coveralls.io/repos/github/clayman74/pytest-postgres/badge.svg?branch=master)](https://coveralls.io/github/clayman74/pytest-postgres?branch=master)
[![PyPI version](https://badge.fury.io/py/pytest-postgres.svg)](https://badge.fury.io/py/pytest-postgres)
[![PyPI](https://img.shields.io/pypi/pyversions/pytest-postgres.svg)]()

pytest-postgres is an plugin for pytest, for adding PostgreSQL database as service into Docker container for tests.

    import psycopg2

    def test_pg_server(pg_server):
        pg_params = pg_server['pg_params']
        with psycopg2.connect(**pg_params) as conn:
            with conn.cursor() as cursor:
                cursor.execute('SELECT version();')

pytest-postgres has been strongly influenced by [pytest-asyncio](https://github.com/pytest-dev/pytest-asyncio/).


Installation
------------

To install pytest-postgres, do:

    (env) $ pip install pytest-postgres


Changelog
---------

0.4.0 (2018-04-03)
~~~~~~~~~~~~~~~~~~
Added --pg-network option. [issue](https://github.com/clayman74/pytest-postgres/pull/5)

0.1.1 (2017-07-20)
~~~~~~~~~~~~~~~~~~
Repair [issue](https://github.com/clayman74/pytest-postgres/issues/2)

0.1.0 (2016-09-15)
~~~~~~~~~~~~~~~~~~
Initial release.
