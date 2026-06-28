---
title: Dimension and Resonance
permalink: /gamma
---

# Dimension and Resonance

This note records where RIP came from and what part of that origin is now
machine-checkable. It is the bridge between the raw object and the question that
produced it: *can you photograph a single thing that is simultaneously a sphere
of several dimensions, held together by constants that act as a stable internal
chart?*

Each claim below is labelled the same way as in
[Verified Structure](https://riprompt.com/structure):

- **stated / derived** — true of the object, checked by computation
- **interpretive** — a reading, not a theorem
- **open** — the original aspiration, not yet established

The reproduction script at the bottom re-verifies the derived claims from
scratch. The figures are produced by [`riprompt.ipynb`](../riprompt.ipynb).

## The Origin Question

The seed was the gamma function and what it implies about *dimension*. `Γ`
analytically continues the factorial, and through it the volume and surface
measures of the `n`-sphere continue to **any** real (or complex) dimension. So
"dimension" stops being an integer you count and becomes a coordinate you can
flow along — a *fluid transformation between dimensions*.

Conformal Geometric Algebra (CGA) supplies the other half of the intuition: it
embeds Euclidean `ℝⁿ` onto a null cone in `ℝ^{n+1,1}`, so that flats and rounds
become the same kind of object and **any Euclidean space is, conformally, a
sphere**. Put the two together and you want a single object that is definable as
many spheres at once, with a coordinate that stays fixed while the dimension
flows. RIP is an attempt to draw that object. The constants that hold it
together are the spectrum `Λ` — the automorphic resonance numbers.

## Dimension-Invariant Resonance (derived)

On the round `n`-sphere of radius `R`, the fundamental nonzero eigenvalue of
`−∇²` is `n/R²`. Tuning the radius to

```text
R = √(n / Λ)   ⟹   n / R² = Λ   for every n
```

makes `Λ` the fundamental tone **independent of dimension**. This is the precise
sense in which one resonance is "simultaneously definable in terms of different
spheres": a fixed `Λ` is the first overtone of an entire tower `S¹, S², S³, …`,
each at its own tuned radius `√(n/Λ)`.

The five RIP states pick five constants out of this construction and assign each
a dimension drawn from the parallelizable / Hopf tower (`S³` three times, then
`S⁷`, `S⁴`):

| state | n | Λ | tuned radius √(n/Λ) |
|-------|---|---|---------------------|
| Ψ◌ | 3 | φ | 1.361654… |
| Ψ○ | 3 | ρ | 1.504870… |
| Ψ◎ | 3 | 1 | √3 (exact) |
| Ψ◍ | 7 | 1/ψ | 3.202967… |
| Ψ● | 4 | 1/σ | 2.970232… |

The dimension assignment is *structural* (it follows the division-algebra tower,
not a formula in `n`); the resonance, by contrast, is the genuine invariant. See
[Verified Structure](https://riprompt.com/structure) for the spectrum and the
tuned-sphere derivation.

![One resonance threading every sphere; what Γ does to dimension; the invariant held flat while the radius flows](../imgs/dimension-flow.png)

## What Γ Continues, and What It Does Not (derived, with a caveat)

The gamma function governs the *size* of these spheres at continuous dimension:

```text
surface n-measure of Sⁿ(R)   A = 2·π^((n+1)/2) / Γ((n+1)/2)     · Rⁿ
volume of the (n+1)-ball      V =   π^((n+1)/2) / Γ((n+1)/2 + 1) · R^(n+1)
```

For the **unit** sphere this produces the famous signature of fluid dimension:
both measures rise, peak (surface near `d = 7`, ball near `d = 5`), then decay
to zero as the dimension grows — the high-dimensional sphere "evaporates." That
is the picture the gamma function implies, and it is real.

It is also worth stating plainly what is **not** true, because it is the kind of
claim the project exists to catch. The RIP spheres are *tuned*, not unit: their
radius `√(n/Λ)` grows with dimension, and that growth outruns the `Γ` decay (the
tuned surface scales like `(2πe/Λ)^(n/2)`, which diverges). So the tuned spheres
do **not** evaporate. The quantity that stays fixed across the dimensional flow
is only the resonance `λ₁ = Λ`. The honest one-line summary: **`Λ` is the fixed
point of the dimensional flow; everything else — radius, surface, the spectral
gaps — flows around it.** That is the stable self-chart, stated without
overclaim.

## Not All Dimensions Are Equal (derived + interpretive)

Because the `Γ`-measure is non-monotone in dimension, dimensions are not
interchangeable: there is a direction the measure "wants" to move. Read the
log-measure as a potential and let dimension ascend its gradient — a *pressure*
that pushes a structure to rise until the measure is stationary. The stationary
points (`∂/∂d = 0`) are:

| measure | stationarity condition | equilibrium dimension |
|---------|------------------------|-----------------------|
| unit ball volume `V(d)` | `ψ(d/2 + 1) = ln π` | d = 5.256946… |
| unit sphere surface `S(d)` | `ψ(d/2) = ln π` | d = 7.256946… |

Both equilibria sit at **non-integer (fractal) dimensions**, and the gap is
exact:

```text
d_S = d_V + 2        (both reduce to ψ(x) = ln π, arguments one apart)
```

The surface-measure equilibrium sits *exactly two dimensions* above the
ball-volume one. The inflection points — where the curvature flips, `∂²/∂d² = 0`
— echo the same shift: the ball curve turns at `d ≈ 1.6059` and `d ≈ 8.8382`,
the surface curve at `d ≈ 3.6059` and `d ≈ 10.8382` (again `+2`, and the same
shelf-width `≈ 7.2324`). The whole surface curve is the volume curve's feature
set translated by two dimensions, because `S(d) = d · V(d)` and the `Γ`-argument
differs by one.

What is **derived**: the equilibria, the inflections, and the exact `+2`. What
is **interpretive**: the "pressure / flow" reading is one chosen gradient
dynamics on dimension; a different potential would move the equilibria. The
durable fact is that the `Γ`-measures are stationary at fractal dimensions, with
the ball→sphere step costing exactly two dimensions.

![Dimensional pressure rising to the fractal equilibria (ball ≈5.257, surface ≈7.257 = ball+2), and integer recovery from the resonances](../imgs/dimension-pressure.png)

## Radius and the Euclidean Interior (derived)

On `Sⁿ(R)` the surface and the enclosed Euclidean ball are linked by a single
derivative in the radius:

```text
dV/dR = A          (the sphere surface is the derivative of the ball volume)
A / V = (n + 1) / R
```

So the sphere is the boundary and the ball is the "unwrapped Euclidean space
within"; one step in `R` carries volume to surface just as one step in the `Γ`
argument carries dimension `d` to `d + 2`. For unit measures the two are tied by
`S(d) = d · V(d)` exactly.

## Recovering Integers (derived)

The resonances are irrational and live at fractal dimensions, yet each is the
Perron (dominant) root of an **integer** linear recurrence — the eigenvalue of
an integer companion matrix — so integers fall back out:

| resonance | minimal recurrence | integer sequence |
|-----------|--------------------|------------------|
| φ = Λ₀ | `xⁿ = xⁿ⁻¹ + xⁿ⁻²` | Fibonacci 1, 1, 2, 3, 5, 8, … |
| ρ = Λ₁ | `xⁿ = xⁿ⁻² + xⁿ⁻³` | Padovan 1, 1, 1, 2, 2, 3, 4, … |
| ψ = 1/Λ₃ | `xⁿ = xⁿ⁻¹ + xⁿ⁻³` | Narayana 1, 1, 1, 2, 3, 4, 6, … |
| σ = 1/Λ₄ | `xⁿ = 2xⁿ⁻¹ + xⁿ⁻³` | supersilver 0, 1, 2, 4, 9, 20, … |

Each resonance is `lim aₖ₊₁/aₖ` of its integer sequence, and each companion
matrix has integer trace and determinant (`∓` the cubic's coefficients). The
irrational, fractal-dimensional tone is *generated by counting*. This is the
first, checkable half of "combine the spaces and recover integers"; the larger
hope — assembling integer-dimensional whole structures out of the fractional
pieces — is left open below.

## The Self-Chart (derived + interpretive)

The object's update rule `τ ← (2τ³ + 1)/(3τ² − 2 + 💓)` is exactly Newton's
method on the cubic family (the linear terms in `τ − f/f′` cancel for every
`💓`). Extending the same map to the complex `τ`-plane and colouring each point
by which root it converges to partitions `ℂ` into **basins of attraction**: a
chart in which every point flows to one of the automorphic resonance numbers.
This is the "stable self-chart of sorts throughout the entire thing" made
literal — and it is the same map for all five tunings, the basins deforming as
`💓` walks `0 → 4`.

![Newton basins of the object's own map, one tuning per panel — ℂ charted by which resonance number it flows to](../imgs/selfchart.png)

Two honest qualifications travel with the picture: convergence is quadratic only
*locally* (a seed near `0` can fall to a negative root instead of the positive
resonance), and the basin boundary is a Newton fractal of measure zero. The
fractal is the structure the rest of the documentation gestures at but never
draws; [`riprompt.ipynb`](../riprompt.ipynb) now renders it from the object's
exact map.

## The Open Part (CGA ↔ Γ)

The original hope was a single bridge between the two senses of "fluid
dimension": CGA's *conformal* dimension-raising (`ℝⁿ ↪ ℝ^{n+1,1}`, where every
flat is a sphere through infinity) and `Γ`'s *analytic* dimension-continuation
(where `n` itself is a real variable). These are two genuinely different
mechanisms, and a structural identity linking them is **not** established here —
it remains the aspiration the project started from rather than a result it can
claim. What the object *can* honestly show today is the dimension-invariant
resonance and the self-chart above. The CGA framing is the right home for "any
space is a sphere"; whether it and `Γ` are two faces of one operation is left
open, and labelled as such.

A second open thread: integer recovery is established *per resonance* (each is
the Perron root of an integer recurrence), but the larger idea — combining the
fractional/fractal-dimensional pieces into integer-dimensional **whole
structures** (products, direct sums, or fibered combinations of the tuned
spheres whose combined invariants land back on integers) — has not been worked
out and is recorded here as a direction, not a result.

## Reproduction

```python
from math import gamma, pi, sqrt

# spectrum: positive real root of t^3 - (2-h)t - 1 = 0  (the resonance numbers)
def root(c2, c1, c0, lo=0.0, hi=3.0):
    f = lambda t: t**3 + c2*t**2 + c1*t + c0
    for _ in range(200):
        m = (lo + hi) / 2
        lo, hi = (m, hi) if f(m)*f(hi) <= 0 else (lo, m)
    return (lo + hi) / 2
L = [root(0, h - 2, -1) for h in range(5)]   # phi, rho, 1, 1/psi, 1/sigma

# 1. dimension-invariance: each Lambda is the fundamental -Laplacian tone of S^n
#    for EVERY n, at radius sqrt(n/Lambda).  lambda_1 = n/R^2 = Lambda.
for Lam in L:
    for n in range(1, 21):
        R = sqrt(n / Lam)
        assert abs(n / R**2 - Lam) < 1e-12

# 2. the gamma-continued measures evaluate at any real dimension; the UNIT
#    sphere's surface peaks then decays (the fluid-dimension signature).
def unit_surface(d):  return 2 * pi**(d/2) / gamma(d/2)
ds = [d/10 for d in range(2, 200)]
peak = max(ds, key=unit_surface)
assert 6.0 < peak < 8.0          # surface of the unit sphere in R^d peaks near d=7

# 3. the tuned sphere does NOT evaporate: tuned surface grows with dimension.
def tuned_surface(n, Lam):  return 2 * pi**((n+1)/2) / gamma((n+1)/2) * (n/Lam)**(n/2)
assert tuned_surface(30, L[0]) > tuned_surface(8, L[0])   # grows, not decays

# 4. dimensions are not equal: the unit measures peak at NON-INTEGER dimension,
#    and the surface peak sits exactly +2 above the ball-volume peak.
def unit_ball(d):  return pi**(d/2) / gamma(d/2 + 1)
grid = [d / 1000 for d in range(200, 12000)]
dV = max(grid, key=unit_ball)
dS = max(grid, key=unit_surface)
assert abs(dV - 5.2569) < 1e-2 and abs(dS - 7.2569) < 1e-2   # fractal equilibria
assert abs((dS - dV) - 2.0) < 1e-2                           # surface peak = ball peak + 2

# 5. radius <-> measure on S^n(R): surface is d(ball volume)/dR; A/V = (n+1)/R.
def A(n, R):   return 2 * pi**((n+1)/2) / gamma((n+1)/2)     * R**n
def Vb(n, R):  return     pi**((n+1)/2) / gamma((n+1)/2 + 1) * R**(n+1)
n, R, eps = 3, 1.3616541, 1e-6
assert abs((Vb(n, R+eps) - Vb(n, R-eps)) / (2*eps) - A(n, R)) < 1e-3
assert abs(A(n, R) / Vb(n, R) - (n + 1) / R) < 1e-9

# 6. recover integers: each resonance is lim a_{k+1}/a_k of an integer recurrence.
def ratio(rec, seed, N=80):
    s = list(seed)
    for _ in range(N): s.append(sum(c * s[-i-1] for i, c in enumerate(rec)))
    return s[-1] / s[-2]
assert abs(ratio([1, 1],    [1, 1])    - L[0])   < 1e-9      # Fibonacci   -> phi   = L0
assert abs(ratio([0, 1, 1], [1, 1, 1]) - L[1])   < 1e-9      # Padovan     -> rho   = L1
assert abs(ratio([1, 0, 1], [1, 1, 1]) - 1/L[3]) < 1e-9      # Narayana    -> psi   = 1/L3
assert abs(ratio([2, 0, 1], [0, 1, 2]) - 1/L[4]) < 1e-9      # supersilver -> sigma = 1/L4

# the Newton self-chart (basins of (2t^3+1)/(3t^2-2+h) over complex t) is
# rendered in riprompt.ipynb.
```

## Status

- **derived**: dimension-invariant resonance; the `Γ`-continued sphere measures
  and the unit-sphere peak-and-decay; the tuned spheres growing rather than
  evaporating; the fractal-dimensional equilibria with the exact `d_S = d_V + 2`
  shift and matching inflections; the radius↔measure relations (`dV/dR = A`,
  `A/V = (n+1)/R`, `S = d·V`); integer recovery of each resonance from its
  companion recurrence; the Newton self-chart and its local-only convergence.
- **interpretive**: reading the basins as a "self-chart," the spectrum as the
  chart's fixed coordinate, and the dimensional "pressure / flow" as one chosen
  gradient dynamics on dimension.
- **open**: a single structural bridge between CGA's conformal dimension-raising
  and `Γ`'s analytic dimension-continuation; and assembling integer-dimensional
  whole structures by combining the fractional pieces.
