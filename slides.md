---
title-slide: false
bibliography: references.bib
csl: vancouver.csl
citeproc: true
theme: serif
background-color: "#ffffff"
transition: slide
navigationMode: linear
hash: true
---

:::: {.columns}
::: {.column width="50%"}

## Sample slides
#### PlaceHolderName
#### Universiti Malaysia Perlis
#### [placeholder@email.com](mailto:placeholder@email.com)

<audio id="bg-music" src="media/audio/sb.m4a" loop></audio>

<div id="audio-credit"
     style="position: absolute; bottom: 40px; right: 20px; font-size: 0.6em; opacity: 0.6;">
  Music: “Adrift” by Scott Buckley (CC BY 4.0)
</div>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    const audio = document.getElementById('bg-music');
    const credit = document.getElementById('audio-credit');

    // hide credit by default
    credit.style.display = 'none';

    const test = new Audio('media/audio/bgm.mp3');

    test.addEventListener('canplaythrough', () => {
      // bgm.mp3 exists → use it, keep credit hidden
      audio.src = 'media/audio/bgm.mp3';
    }, { once: true });

    test.addEventListener('error', () => {
      // bgm.mp3 missing → sb.m4a will play → show credit
      credit.style.display = 'block';
    }, { once: true });

    document.addEventListener('click', () => {
      if (Reveal.getIndices().h === 0) {
        audio.volume = 0.5;
        audio.play();
      }
    }, { once: true });

    Reveal.on('slidechanged', (event) => {
      if (event.indexh > 0) { audio.pause(); }
      else { audio.play(); }
    });
  });
</script>

:::

::: {.column width="50%"}
![](media/pics/logo1.png)
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Slide one
**Key Concepts:**
- Energy conservation per @carnot1824.
- $\Delta U = Q - W$
:::

::: {.column width="50%"}
![](media/pics/sample.png)
:::
::::

---

<span class="slide-title" data-title="My Hidden Slide Name"></span>

![](media/pics/wide.jpeg)

---

:::: {.columns}
::: {.column width="50%"}
### The Master Equation
The fundamental relation of thermodynamics:

$$\Delta U = Q - W$$

The work done $W$ is positive when the system expands against an external pressure.
:::

::: {.column width="50%"}
<video data-src="media/videos/sample.mp4" data-autoplay loop muted width="100%"></video>
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Visualizing the Gas Law
**Interactive Model:**

- P, V, and T relationships.
- Use the slider to adjust pressure.
- Observe the phase boundary.
:::

::: {.column width="50%"}
<iframe 
  data-src="media/plots/sample.html" 
  width="100%" 
  height="500px" 
  style="border:none;" 
  scrolling="no">
</iframe>
:::
::::

---

# Bibliography
<div id="refs"></div>

---

:::: {.columns}
::: {.column width="50%"}
### Math Scores Distribution

This histogram illustrates the distribution of Math scores within the dataset.

- **X-axis (Math Score):** Represents the range of math scores.
- **Y-axis (Frequency):** Shows how many students fall into each score range.

Observe the spread and central tendency of the scores to understand student performance.
:::

::: {.column width="50%"}
<iframe
  data-src="media/plots/math_scores_histogram.html"
  width="100%"
  height="500px"
  style="border:none;"
  scrolling="no">
</iframe>
:::
::::
---

# Key Statistics for Machine 1

## Conditions:
- **Machine:** 1
- **Temperature:** 303
- **Pressure:** 100

## Part Length (mm)
- **Mean:** 51.7612
- **Median:** 51.7723
- **Standard Deviation:** 0.9821

## Part Resistance (Ohms)
- **Mean:** 5.5064
- **Median:** 5.5015
- **Standard Deviation:** 0.353


---

:::: {.columns}
::: {.column width="50%"}
### Part Length Xbar.one Control Chart

This chart monitors the individual observations of 'Part Length' over time.

- **Blue Dashed Line:** Represents the overall mean of the part length.
- **Red Solid Lines:** Indicate the Upper Control Limit (UCL) and Lower Control Limit (LCL), set at 3-sigma from the mean.
- **Points:** Each point is an individual measurement.

Points falling outside the control limits suggest an out-of-control process, requiring investigation.
:::

::: {.column width="50%"}
<iframe
  data-src="media/plots/part_length_xbar_one_chart.html"
  width="100%"
  height="500px"
  style="border:none;"
  scrolling="no">
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Part Resistance Xbar.one Control Chart

This chart monitors the individual observations of 'Part Resistance' over time.

- **Blue Dashed Line:** Represents the overall mean of the part resistance.
- **Red Solid Lines:** Indicate the Upper Control Limit (UCL) and Lower Control Limit (LCL), set at 3-sigma from the mean.
- **Points:** Each point is an individual measurement.

Points falling outside the control limits suggest an out-of-control process, requiring investigation.
:::

::: {.column width="50%"}
<iframe
  data-src="media/plots/part_resistance_xbar_one_chart.html"
  width="100%"
  height="500px"
  style="border:none;"
  scrolling="no">
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Part Length Xbar.one Control Chart - Machine 1 (P=200, T=338)

This chart monitors the individual observations of 'Part Length' over time for Machine 1 under the specified conditions (Pressure = 200, Temperature = 338).

- **Blue Line:** Individual part length measurements.
- **Green Dashed Line:** Represents the overall mean of the part length.
- **Orange Solid Lines:** Indicate the Upper Control Limit (UCL) and Lower Control Limit (LCL), set at 3-sigma from the mean.
Points falling outside the control limits suggest an out-of-control process, requiring investigation.
:::

::: {.column width="50%"}
<iframe
  data-src="media/plots/m1_temp338_pres200_partlength_control.html"
  width="100%"
  height="500px"
  style="border:none;"
  scrolling="no">
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Part Resistance Xbar.one Control Chart - Machine 1 (P=200, T=338)

This chart monitors the individual observations of 'Part Resistance' over time for Machine 1 under the specified conditions (Pressure = 200, Temperature = 338).

- **Blue Line:** Individual part resistance measurements.
- **Green Dashed Line:** Represents the overall mean of the part resistance.
- **Orange Solid Lines:** Indicate the Upper Control Limit (UCL) and Lower Control Limit (LCL), set at 3-sigma from the mean.
Points falling outside the control limits suggest an out-of-control process, requiring investigation.
:::

::: {.column width="50%"}
<iframe
  data-src="media/plots/m1_temp338_pres200_partresistance_control.html"
  width="100%"
  height="500px"
  style="border:none;"
  scrolling="no">
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 1 Analysis
**Conditions:**
- Temperature: 338K
- Pressure: 200kPa

**Findings:**
- Control Chart for Part Length shows the stability of the process.
- The red lines indicate the UCL and LCL.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/m1_length_chart.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 2 Analysis
**Conditions:**
- Temperature: 338K
- Pressure: 200kPa

**Findings:**
- Control Chart for Machine 2 is displayed on the right.
- This chart tracks the consistency of Part Length under specified conditions.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/m2_control_chart.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 3 Analysis
**Conditions:**
- Temperature: 338K
- Pressure: 200kPa

**Findings:**
- Control Chart for Machine 3 is displayed on the right.
- This visualization helps in determining if Machine 3 is in control.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/m3_control_chart.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::
