# Focus Calculators

Interactive, browser-based calculators that model how interruptions reduce deep work capacity during a standard workday.

## What this project is

This repository contains a small static web app (no backend) with:

- A landing page (`index.html`)
- A **Focus Capacity Calculator** (`focus-capacity-calculator.html`)
- A **Productivity Perception Calculator** (`productivity-perception-calculator.html`)

The calculators simulate interruption-driven workdays and help explain why frequent context switching makes sustained focus difficult.

## Calculators

### 1) Focus Capacity Calculator

Explores focus capacity using tunable parameters:

- **λ (lambda):** interruptions per hour
- **Δ (delta):** recovery time after interruptions (minutes)
- **θ (theta):** minimum uninterrupted block needed for meaningful work (minutes)

Outputs include:

- Expected capacity (count of complete `θ`-sized blocks)
- Total focus time
- Total recovery time
- Longest uninterrupted block
- A timeline visualization of an 8-hour day

The core idea represented in the UI is:

`C(θ) = Σ ⌊dᵢ / θ⌋`

where `dᵢ` are uninterrupted focus block durations and partial blocks do not count toward capacity.

### 2) Productivity Perception Calculator

Estimates whether a person is likely to *feel productive* based on:

- Interruption rate (λ)
- Recovery time (Δ)
- Personal daily focus target (hours)

Outputs include:

- Expected focus hours across interruption-rate scenarios
- Comparison against the selected productivity target
- Daily interruption estimates
- A recommendation for the maximum interruption rate to hit the target

## How to use

1. Open `index.html` in a browser.
2. Choose a calculator.
3. Move sliders to reflect your real work environment.
4. Use the visuals and metrics to evaluate focus impact and adjust expectations or work protections.

## Implementation notes

- Pure HTML/CSS/JavaScript (static files only)
- No build step required
- No package manager or runtime dependencies

## Source / inspiration

This project is based on:

- **Can Duruk**, *The Math of Why You Can't Focus at Work*  
  https://justoffbyone.com/posts/math-of-why-you-cant-focus-at-work/

## License

See `LICENSE`.
