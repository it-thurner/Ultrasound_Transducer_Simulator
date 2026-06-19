# Ultrasound Transducer Simulator

A MATLAB tool for the design and optimization of ultrasonic transducers. It models the
transducer with a Mason equivalent-circuit / transmission-line approach to compute the
**electrical** input impedance *Z(f)* of a layered stack, and synthesizes discrete L-C
matching networks for electrical impedance matching to a **50 Ω front-end**.

This is *electrical* impedance matching — not *acoustic* impedance matching. The two are
independent concepts and are not used interchangeably here.

Impedance data can come from either the built-in Mason simulation (parameterized by
geometry and material properties) or directly from a VNA measurement.

## Requirements
- MATLAB (R2019b or newer recommended)
- Signal Processing Toolbox (`findpeaks`)
- Curve Fitting Toolbox (`smooth`)

## Usage
1. Open `US_Simulation_Programm.m` in MATLAB.
2. Define the transducer stack in the `US = struct(...)` line near the top.
3. Uncomment one of the `plot_*` calls (e.g. `plot_freq_domain`, `plot_matching`,
   `plot_matching_compare`) to run the desired analysis.
4. For VNA-based analysis, update the hard-coded CSV paths (currently `C:\export\...`)
   to point to your own exported VNA measurements.

## Citation
If you use this tool, please cite it — see the **Cite this repository** button
(generated from `CITATION.cff`).

## License
Released under the MIT License — see [LICENSE](LICENSE).

## Author
Stephan Thurner — Institute of Health Care Engineering (IHCE), TU Graz.
