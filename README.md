# Integer Prime Structure Visualizer ✨📊
<img width="1494" alt="image" src="https://github.com/user-attachments/assets/3e3d3f73-97c7-4672-b07d-bded7bd9a8e2" />


## Overview

This project provides an interactive web application for exploring the fascinating structure hidden within the integers, revealed through their unique prime factorizations. Based on the fundamental theorem of arithmetic, every integer `n > 1` can be written as `n = p₁^e₁ * p₂^e₂ * ... * p_k^e_k`. This visualizer maps integers onto various 2D and 3D coordinate systems based on properties derived from these prime factors (`pᵢ`) and their exponents (`eᵢ`).

By plotting integers according to different structural summaries (like peak exponent intensity, total factor volume, or factor variety), the tool reveals underlying mathematical patterns, relationships, statistical distributions, and connections to core number theory concepts.

## Conceptual Framework: Numbers as Relationships

Instead of viewing integers merely as quantities, this tool embraces a conceptual perspective where each integer embodies its unique prime factorization – a specific **"Pattern of Relatedness"** to the fundamental prime building blocks. The exponents `{eᵢ}` quantify the strength of these relationships.

The different visualization views map these fundamental "Patterns" onto geometric spaces using summary statistics:

*   **Peak Intensity:** The maximum exponent (`max{eᵢ}`).
*   **Total Volume:** The sum of exponents (`Ω(n) = Σeᵢ`).
*   **Variety:** The number of distinct prime factors (`ω(n) = k`).

The resulting plots allow us to visually compare these structural profiles and observe the **"meta-relationships"** – the underlying mathematical laws and statistical tendencies governing how these Patterns are structured and relate to each other.

## Features

*   **Multiple Visualization Views:**
    *   **ISG (Intensity vs. Volume):** `X = max{eᵢ}`, `Y = Ω(n)`
    *   **DFG (Variety vs. Intensity):** `X = ω(n)`, `Y = max{eᵢ}`
    *   **OmegaOmega (Variety vs. Volume):** `X = ω(n)`, `Y = Ω(n)`
    *   **Combined 3D:** `X = ω(n)`, `Y = max{eᵢ}`, `Z = Ω(n)`
*   **Interactive Plots:** Powered by Plotly.js, supporting zooming, panning, and hovering to view details.
*   **Flexible Input:** Visualize a single integer or a range of integers (e.g., `1-1000`).
*   **Highlighting:**
    *   Highlight a specific integer by clicking its point or entering it in the input box.
    *   Highlight categories of numbers (Primes, Prime Powers, Perfect Squares, Square-free, Perfect, Abundant, Deficient).
*   **Mathematical Overlays:** Key mathematical lines/regions (e.g., `y=x`, `ω=1`, Square-free region) are drawn on relevant plots for context.
*   **Statistical Information:** Displays calculated vs. theoretical statistics related to:
    *   Density of square-free/cube-free numbers (linked to `ζ(2)`, `ζ(3)`).
    *   Distribution of distinct prime factors (linked to Erdős–Kac theorem, `log(log N)`).
*   **Liouville Function (λ(n)) Color Mode:** Optionally color points based on the parity of `Ω(n)`.
*   **Axis Scaling:** Choose between Linear and Logarithmic scales for 2D plot axes.
*   **Detailed Information Panel:** Clicking a point or highlighting a number shows its factorization, coordinates in all views, number-theoretic metrics (`ω(n)`, `Ω(n)`, `λ(n)`, `d(n)`, `σ(n)`), and special properties.
*   **In-App Explanations:** Includes sections detailing the Conceptual Framework and interpreting the Mathematical Insights revealed by the plots.

## Mathematical Insights (Explained in App)

The application includes a dedicated section explaining how specific mathematical phenomena manifest visually in the different views, including:

*   **Exponentiation & Scaling Rays:** How `m^k` relates to `m` geometrically (ISG View).
*   **Liouville Function & Parity:** How `λ(n)` relates to the Y-axis in ISG/OmegaOmega views.
*   **Multiplication Rules:** How coordinates combine when multiplying numbers.
*   **Structural Spread:** The meaning of `Ω(n) - max{eᵢ}` and `Ω(n) - ω(n)`.
*   **Density & Zeta Function:** Connections between power-free numbers and `ζ(s)`.
*   **Distinct Factor Distribution:** Links to the Erdős–Kac theorem.

This is a pure frontend application. No build process or server is required.

1.  **Download or Clone:** Get the project files (specifically the HTML file and any associated CSS/JS if separated, though currently it's self-contained).
2.  **Open HTML File:** Open the `index.html` (or the relevant HTML file name) directly in your web browser (e.g., Chrome, Firefox, Edge, Safari).

**Note on Performance:** Calculating prime factorizations for large ranges of large numbers can be computationally intensive and may take time or cause the browser to become temporarily unresponsive. The current implementation uses trial division, suitable for numbers up to roughly 1 million within reasonable time. A maximum range limit (e.g., 5000 numbers) is enforced to prevent browser freezes.

## How to Use

1.  **Input Range:** Enter a single positive integer or a range using a hyphen (e.g., `50`, `1-500`) into the "Integer(s) Range" field.
2.  **Visualize:** Click the "Visualize" button. The plots will update (this may take a moment for larger ranges).
3.  **Explore Plots:**
    *   Use your mouse to **zoom** (scroll wheel or pinch), **pan** (click and drag), and **rotate** (3D view).
    *   **Hover** over points to see a tooltip with the integer `n`, its coordinates in that view, and its `λ(n)` value.
    *   **Click** on a point to select its integer, display its full details in the "Integer Analysis" panel below, and highlight it across all plots.
4.  **Highlight Specific Integer:** Enter a positive integer in the "Highlight Integer" box. Its details will appear in the panel below, and its corresponding point (if plotted) will be highlighted.
5.  **Highlight Categories:** Select a category (e.g., "Primes") from the dropdown to highlight all corresponding integers in the plots. Select "None" to clear category highlights.
6.  **Color Mode:** Choose "Default by View" or "By Liouville Function λ(n)" to change point colors based on `Ω(n)` parity (requires re-visualization).
7.  **Axis Scaling:** Use the "Lin/Log" selectors below each 2D plot header to change axis scales (requires re-visualization).
8.  **Interpret:** Use the plot overlays, statistical displays, and the "Mathematical Insights" section below the plots to understand the patterns you observe.

## Future Improvements Potential

*   Implement Web Workers for background calculations to improve UI responsiveness.
*   Integrate more advanced prime factorization algorithms for larger numbers.
*   Implement brushing and linking between plots.
*   Add plot data/image export functionality.
*   Introduce data aggregation techniques (heatmaps, density plots) for very large ranges.
*   Add filtering controls for plotted data.
*   Offer preset ranges or interesting number sets.
*   Enhance 3D view controls and projections.
