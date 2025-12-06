

# **Thermal Conductivity: Modeling Heat Transfer Through Real Materials** 
![alt text](<Photos/Material tests.png>)

When modern devices heat up, whether it’s a phone during charging, a laptop under load, or a battery pack, design and hardware engineers rely on how fast heat moves through different materials.
Understanding that behavior is the difference between a device that performs well and one that fails early.

This project explores that same problem at a smaller scale. Using data science and physics principles, I measured how aluminum foil, plastic, and cardboard conduct heat and built a mathematical model that reproduces their thermal behavior. 

**Even though this experiment is simple and small in scale, the insights map directly to real-world engineering challenges in electronics cooling and energy systems.**

# **What This Project Does**
![alt text](<Photos/TC Lab Diagram.png>)
* Using a modified Arduino microcontroller, collects temperature data from a heated surface using different material samples
* Computes  heat-transfer quantities: conduction, convection, and radiation
* Builds a numerical model that estimates how each material heats over time
* Compares predicted temperature curves to actual measurements
* Extracts material behavior and properties like thermal conductivity


# **How to Explore This Project**

- `Data/` – Raw temperature measurements from each material test
- `Photos/` – Experiment and setup images
- `Final_Project.ipynb` – Full analysis and visualizations



# **The Physics Behind It**

The conduction relationship:

$$
Q = kA\frac{T_2 - T_1}{d}
$$

is combined with the convection and radiation heat-loss terms:

$$
q_{\text{conv}} = hA(T_\infty - T_2)
$$

$$
q_{\text{rad}} = \sigma \varepsilon A\left((T_\infty + 273.15)^4 - (T_2 + 273.15)^4\right)
$$

These flow into the energy balance:

$$
\frac{dT_2}{dt} = \frac{q_{\text{cond}} + q_{\text{conv}} + q_{\text{rad}}}{m c_p}
$$

This differential equation is solved numerically and compared against measured temperature curves for each material.

Even though the math looks complex, the big idea is simple:
**All materials move heat differently, and you can measure and model that difference directly.**



# **Results** 

* **Aluminum foil** transferred heat the fastest, which makes sense being a metal conductor.
* **Plastic** fell in the middle, warming steadily but slower than aluminum.
* **Cardboard** acted as an insulator and dramatically slowed heat transfer.

What makes this useful is not just identifying which material is an insulator or a conductor, but showing that the model mirrors the experiment.


# **Why This  Matters**

This project demonstrates how experimental data, physics, and Python can be combined to analyze a real system and solve practical problems. It highlights and reinforces skills that apply to engineering, data science, and applied research:

* Working with real sensor data
* Translating physical laws into a mathematical model
* Implementing and validating simulations
* Communicating results through structured analysis


*I had a lot of fun working on this. This project was guided and inspired by the open-source Temperature Control Lab (TCLab) educational kit from APmonitor.com, which provides accessible tools for exploring heat-transfer principles through hands-on experiments.*

