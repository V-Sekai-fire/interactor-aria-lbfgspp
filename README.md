# interactor-aria-lbfgspp

An Elixir library that drives the LBFGS++ limited-memory quasi-Newton optimizer through a NIF.

## What it is for

It minimizes an objective either from gradients the caller supplies or, when the caller has only
objective values, from gradients estimated over its observation history through a suggest and
observe loop. Each optimizer instance lives in a GenServer and is persisted with Ecto.
`examples/` holds runnable scripts for both interfaces.

## Build and test

```sh
mix deps.get
mix test
```

Compiling builds the NIF against the optimizer and linear algebra headers vendored under
`thirdparty/`.

## Licence

MIT; see `LICENSE`. The vendored libraries keep their own licences under `thirdparty/`.
