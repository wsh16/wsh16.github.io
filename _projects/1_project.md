---
layout: page
title: Sensorless Control
description: Sensorless control of linear motors.
img: assets/img/scheme.jpg
importance: 1
category: Projects
---

The thesis of my master's degree is on sensorless control of linear motors. It is a two-year long research with theoretical innovation and experimental verification. The work is carried out in cooperation with a doctoral student Ziyan Zhao.

## Importance of sensorless control
Permanent magnet linear synchronous motors (PMLSMs) has been wildly used in industry, and position feedbacks are often needed for their commutation and close-loop control. However, the use of position sensors presents certain drawbacks and limitations:
1. Position sensors will increase the cost and difficulty in manufacturing PMLSMs, against their spread in industry. 
2. The addition of sensors will increase the motor system complexity and reduce the system robustness, particularly when working in an environment with oil or dust.
3. In some special motors with extremely limited size or extremely long strokes, traditional position sensors are difficult to apply.

Therefore, it is meaningful to realize motion control of PMLSMs without position sensors. 

<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.html path="assets/img/PositionSensors.jpg" title="Position Sensors" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/Conditions.jpg" title="Examples when position sensors are not preferred" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Position sensors and when they are not preferred.
</div>

---

## Our Sensorless Control Technology

We designed a sensorless control algorithm based on flux estimation. The basic principle is that the flux signal can be obtained by electrical signals and it is related to rotor position. So, by using current sensors (which is already inside most commercial motor drivers) we can decode the rotor position. To realize high accuracy flux estimation, we proposed an reciprocal flux correction method. The scheme of sensorless control system is shown as below.

<div class="col-sm mt-3 mt-md-0">
    {% include figure.html path="assets/img/scheme.jpg" title="scheme of sensorless control" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
    Scheme of sensorless control
</div>

---

## Experiment Results

We conduct several experiments on a commercial PMLSM to verify the given sensorless control algorithm and compared our method with others[1-2].

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/ExperimentSet.jpg" title="Experiment Set" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/AIM_exp.jpg" title="Experiment Results" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Experiment set and some of the results.
</div>

The above figure gives the structure of our experiment set and some of the results. Compared to other methods (M1 and M2), our proposed method (M3) can reduce position estimation error on sinusoidal speed trajectories by 70%.

[1] J. Hu and B. Wu, “New integration algorithms for estimating motor flux over a wide speed range,” *IEEE Trans. Power Electron.*, vol. 13, no. 5, pp. 969–977, Sep. 1998.

[2] R. Zhao, Z. Xin, P. C. Loh, and F. Blaabjerg, “A novel flux estimator based on multiple second-order generalized integrators and frequency-locked loop for induction motor drives,” *IEEE Trans. Power Electron.*, vol. 32, no. 8, pp. 6286–6296, Aug. 2017.

<video width="720" height="480" controls>
  <source src="motor_sensorless.mp4" type="video/mp4">
  <source src="motor_sensorless.webm" type="video/webm">
  <object data="motor_sensorless.mp4" width="720" height="480">
    <embed src="motor_sensorless.swf" width="720" height="480">
  </object>
</video>

---

## Presentation on 2022 AIM

The work was accepted by the 2022 IEEE/ASME International Conference on Advanced Intelligent Mechatronics (AIM) and I made an oral presentation. Here is the record of the presentation.

<video width="720" height="480" controls>
  <source src="AIM_pre.mp4" type="video/mp4">
  <source src="AIM_pre.webm" type="video/webm">
  <object data="AIM_pre.mp4" width="720" height="480">
    <embed src="AIM_pre.swf" width="720" height="480">
  </object>
</video>

