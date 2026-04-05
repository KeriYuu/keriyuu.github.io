---
layout: default
title: Fractal
permalink: /thoughts/fractal/
date: 2025-04-24
---

<script>
window.MathJax = {
  tex: {
    inlineMath: [['$', '$'], ['\\(', '\\)']],
    displayMath: [['$$', '$$'], ['\\[', '\\]']]
  }
};
</script>
<script async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

[Home](/) | [Thoughts](/thoughts/) | [Gallery](/gallery/)

## Fractal
<small>{{ page.date | date: "%B %Y" }}</small>

Nassim Nicholas Taleb points out in [The Black Swan](https://en.wikipedia.org/wiki/The_Black_Swan:_The_Impact_of_the_Highly_Improbable) that seemingly similar market fluctuations may conceal entirely different underlying drivers. 

I wrote a simple program ([GitHub Repository](https://github.com/KeriYuu/fractal-game)) to simulate such elegant self-similar structures:  

In the complex iteration formula:

$$
z_{n+1} = z_n^2 + c
$$

If the sequence doesn't diverge, the constant $c$ belongs to the Mandelbrot set.  
When fixing $c$ and iterating $z_{n+1} = z_n^2 + c$, all initial $z_0$ points whose sequences remain bounded form the Julia set.  

| ![Mandelbrot](/images/mandelbrot.png){: width="300px" } | ![Julia](/images/julia.png){: width="300px" } |
|:-------------------------------------------------------:|:------------------------------------------------:|
| Mandelbrot Set                                         | Julia Set                                         |


Darker colors in the figure indicate more iterations required.  

The fractal boundary marks the division between "stable orbits" and "escape trajectories" – we observe how slight perturbations in initial values can lead to radically different outcomes (convergence or divergence).
