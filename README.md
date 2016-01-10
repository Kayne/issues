# Issues

This is simple program based on Dave Thomas "Programming Elixir" book.
It's showing n issues of the provided github repository. It's sending a query to GitHub API, downloads JSon reseponse and converts into nice ASCII table.

##  Installation

Just get this repository and run escript.build to make runnable erlang package:

```sh
$ mix escript.build
```

The `issues` package will be created and runnable as described below. If you prefer to run in iex you can always do that:

```ssh
$ mix run -e 'Issues.CLI.main(["elixir-lang", "elixir"])'
```

or:

```ssh
$ iex -S mix
iex(1)> Issues.CLI.main(["elixir-lang", "elixir"])
```

## Usage

General usage:

```sh
$ ./issues <user> <project> [count | 4]
```
For example to get 10 issues from elixir-lang:
```sh
$ ./issues elixir-lang elixir 10
```

## Dependencies

Issues uses few libraries:

* [httpoison](https://github.com/edgurgel/httpoison) - HTTP Client, ~> 0.8.0
* [poison](https://github.com/devinus/poison) - JSON library, ~> 1.5

```elixir
defp deps do
  [
    { :httpoison, "~> 0.8.0" },
    { :poison, "~> 1.5" }
  ]
end
```

## Todo

- More tests
- Better documentation