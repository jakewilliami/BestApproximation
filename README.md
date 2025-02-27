<h1 align="center">
    BestApproximation.jl
</h1>

<!-- [![Stable](https://img.shields.io/badge/docs-stable-blue.svg)](https://jakewilliami.github.io/BestApproximation.jl/stable) -->
[![Dev](https://img.shields.io/badge/docs-dev-blue.svg)](https://jakewilliami.github.io/BestApproximation.jl/dev)
[![CI](https://github.com/invenia/PkgTemplates.jl/workflows/CI/badge.svg)](https://github.com/jakewilliami/BestApproximation.jl/actions?query=workflow%3ACI)
[![Code Style: Blue](https://img.shields.io/badge/code%20style-blue-4495d1.svg)](https://github.com/invenia/BlueStyle)
![Project Status](https://img.shields.io/badge/status-maturing-green)

Given a potentially very large number, it is sometimes nice to approximate this.  To find the "best", or "nicest" approximation, usually we restrict the base of an exponent, so that your given number ``n`` is approximately ``b^x``.  The idea is that ``b^x`` is nicer looking than your input.

This is a very small package exporting a function to find `b` and `x`, given a range `b` can be in.

## Quick Start

```julia
julia> using BestApproximation

julia> best_approx(123, 20)  # The second parameter is the maximum number for the base (i.e., it returns 11^2, with 11 < 20).  You can also specify the range of the exponent, but this variant is much slower.
(11, 2)

julia> ^(best_approx(123, 20)...)  # Notice how 11^2 approximates to 121---only 2 numbers off the given number.
121
```

## Citation

If your research depends on BestApproximation.jl, please consider giving us a formal citation: [`citation.bib`](./citation.bib).
