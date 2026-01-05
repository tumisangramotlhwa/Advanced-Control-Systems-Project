# Advanced-Control-Systems-Project

Problem:


Why it matters:


Approach:

Leveraged Symmetric Root Locus-informed LQR design to systematically translate time-domain specifications into optimal state weighting, ensuring fast, critically damped responses while minimizing steady-state error

Incorporated discrete-time Kalman filtering (LQG) for optimal state estimation under noisy measurements, applying the separation principle to independently tune controller and observer while maintaining guaranteed closed-loop stability

Implemented constrained MPC with receding horizon optimisation, integrating input/state constraints and prediction horizons to balance aggressive tracking with actuator limitations and achieve robust, real-time reference following

Key Insight:

Achieving precise control requires careful trade-offs between state tracking performance and control effort, systematically tuned through Q/R ratios in LQR and W/V ratios in Kalman filtering

Augmenting the system to include integrators and disturbance models allows principled application of the Internal Model Principle for zero steady-state error and predictable disturbance rejection

Optimal performance emerges from holistic integration of control, estimation, and predictive strategies, highlighting the value of rigorous theoretical foundations applied to practical nonlinear systems

Tuning parameters such as MPC horizon length, input change penalties, and observer gains directly impact transient behaviour and robustness, demonstrating that detailed engineering choices materially affect system-level performance

Result:

Achieved near-zero steady-state error across all controllers with maximum overshoot limited to 3–4° and sub-second settling times

LQG observer accurately estimated states under process and measurement noise, with estimation error <1.5° even during reference reversals

MPC with receding horizon and constraints maintained reference tracking with negligible overshoot, demonstrating predictive control under physical input limits

Input signals remained well within actuator limits, confirming robust, energy-efficient operation without saturation
