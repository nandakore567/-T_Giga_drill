# Ordiva Universe Theory

> Time reversal is not a paradox—it’s a wave.  
> This repository contains the theoretical framework, Python simulation, and visualizations  
> for the structural entropy model: **Ordiva(t) = S₀·cos(ωt)·(–1)^{⌊t/T⌋}**

---

## Overview

This theory proposes a cyclic structural entropy wave called **Ordiva**,  
explaining time symmetry, antimatter phases, and consciousness perception.

- PDF: [Ordiva_Universe_Theory_FINAL_COMPLETE.pdf](./Ordiva_Universe_Theory_FINAL_COMPLETE.pdf)
- DOI: [10.5281/zenodo.15336187](https://doi.org/10.5281/zenodo.15336187)
- Author: [@T_Giga_Drill](https://x.com/T_Giga_Drill)

---

## Code: Ordiva Simulation (Python)

```python
import numpy as np
import matplotlib.pyplot as plt

def ordiva(t, S0=1.0, omega=1.0, T=2*np.pi):
    phase = (-1)**np.floor(t / T)
    return S0 * np.cos(omega * t) * phase

t = np.linspace(-20, 20, 1000)
S = ordiva(t)
plt.plot(t, S)
plt.title("Ordiva(t) – Structural Entropy Wave")
plt.grid(True)
plt.show()

