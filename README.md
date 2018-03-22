# Subtitles

**This library provides several tools for manipulating and converting subtitles**

## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed
by adding `subtitles` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:subtitles, "~> 0.1.0"}
  ]
end
```

Documentation can be generated with [ExDoc](https://github.com/elixir-lang/ex_doc)
and published on [HexDocs](https://hexdocs.pm). Once published, the docs can
be found at [https://hexdocs.pm/subtitles](https://hexdocs.pm/subtitles).

## Usage

All functions convert all line endings to LF before operations are done.

### Functions

**get_format(subtitle)**

Returns the subtitle format as an atom, defaults to `:unknown`

```
subtitle = "WEBVTT\n\n..."
get_format(subtitle) -> :vtt

subtitle = "1\r\n..."
get_format(subtitle) -> :srt

subtitle = "Anything else..."
get_format(subtitle) -> :unknown
```
