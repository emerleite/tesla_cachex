# TeslaCache

[![Build Status](https://travis-ci.org/emerleite/tesla_cache.svg?branch=master)](https://travis-ci.org/emerleite/tesla_cache)
[![Coverage Status](https://coveralls.io/repos/github/emerleite/tesla_cache/badge.svg?branch=master)](https://coveralls.io/github/emerleite/tesla_cache?branch=master)
[![codecov](https://codecov.io/gh/emerleite/tesla_cache/branch/master/graph/badge.svg)](https://codecov.io/gh/emerleite/tesla_cache)
[![Module Version](https://img.shields.io/hexpm/v/tesla_cache.svg)](https://hex.pm/packages/tesla_cache)
[![Hex Docs](https://img.shields.io/badge/hex-docs-lightgreen.svg)](https://hexdocs.pm/tesla_cache/)
[![Total Download](https://img.shields.io/hexpm/dt/tesla_cache.svg)](https://hex.pm/packages/tesla_cache)
[![License](https://img.shields.io/hexpm/l/tesla_cache.svg)](https://github.com/emerleite/tesla_cache/blob/master/LICENSE)
[![Last Updated](https://img.shields.io/github/last-commit/emerleite/tesla_cache.svg)](https://github.com/yyy/tesla_cache/commits/master)

TeslaCache is a Basic Cache Middleware for [Tesla](https://hex.pm/packages/tesla).
It will cache only GET requests for X milliseconds.

## Installation

Add `:tesla_cache` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:tesla_cache, "~> 1.1.0"}
  ]
end
```

## Usage

```elixir
defmodule GoogleClient do
  use Tesla

  plug Tesla.Middleware.Cache, ttl: :timer.seconds(2)
end
```

## License

The source code is under the MIT License. Copyright (c) 2017- Emerson Macedo.
