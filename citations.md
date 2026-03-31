# Research References — Mapped to Pipeline Layers

All papers accessed via VTU IEEE Xplore consortium access, March 2026.

---

## Layer 2 — Anomaly Detection

**Paper 6** — Application of Temporal Neural Networks in Anomaly Detection and Restoration of Industrial Carbon Emission Data  
*Luo et al., Zhejiang Zhongxin Electric Power Engineering Construction Co., 2025*  
*Conference: IDSAC 2025 | DOI: 10.1109/IDSAC65763.2025.11170195*  
→ Justifies BiGRU-Attention autoencoder architecture for industrial anomaly detection.  
→ Reports 0.92 F1-score, 18.4% improvement over LSTM baseline.  
→ Confirms event-triggered sampling reduces data acquisition by 35%.

---

## Layer 3 — LSTM Trend Model

**Paper 9** — Prediction of Life Expectancy of Electronic Components Estimated by Neural Network  
*Shterev, Momchev & Asenov, Technical University of Sofia, 2023*  
*Conference: ICEST 2023 | DOI: 10.1109/ICEST58410.2023.10187261*  
→ Validates FFNN-based remaining useful life prediction on NASA PCoE IGBT dataset.  
→ Demonstrates 5.7–10.4% prediction error depending on training sample size.  
→ Confirms neural network outperforms classical statistical regression for RUL.

---

## Layer 4 — RUL Estimation (GaN FET / MOSFET)

**Paper 7** — Support Vector Regression Assisted Auxiliary Particle Filter based Remaining Useful Life Estimation of GaN FET  
*Haque & Choi, Mississippi State University, 2018*  
*Conference: IEEE APEC 2018 | DOI: 10.1109/APEC.2018.8341250*  
→ Core algorithm for Layer 4 RUL estimation of power semiconductors.  
→ Uses RdsON as fault precursor (IEC 60747-9-2007 standard: 10% increase = failure).  
→ SVR-APF hybrid achieves 7–11% RUL error across hybrid linear/nonlinear trajectories.  
→ Handles abrupt operating condition changes — validated on 16 GaN FETs under power cycling.

**Paper 8** — Reliability Monitoring and Predictive Maintenance of Power Electronics with Physics and Data Driven Approach Based on Machine Learning  
*Cui, Hu, Tallam et al., Rockwell Automation, 2023*  
*Conference: IEEE APEC 2023 | DOI: 10.1109/APEC43580.2023.10131151*  
→ Weibull degradation model: R(t) = exp(−(t/α)^β).  
→ Ensemble ML approach with dynamic weight updating — no prior failure data required.  
→ Validated on NASA MOSFET aging dataset (RdsON as reliability indicator).  
→ K-means clustering for automated anomaly pattern classification.

---

## Layer 4 — Failure Physics (Capacitor)

**Paper 3** — An Investigation on the Dielectric, Ferroelectric Properties and Failure Mechanism for the 0805 X7R MLCC  
*Wang, Sun, Zhang et al., SIAT Chinese Academy of Sciences, 2023*  
*Conference: ICEPT 2023 | DOI: 10.1109/ICEPT59018.2023.10491963*  
→ Establishes oxygen vacancy migration as the primary MLCC failure mechanism.  
→ Schottky barrier drops from 0.6 eV to 0.4 eV after aging — measurable via impedance.  
→ Justifies AD5933 impedance spectroscopy as capacitor health precursor in our pipeline.

---

## Layer 4 — Failure Physics (PCB / Solder Joints)

**Paper 1** — Failure Analysis for Micro-Short Circuit between Two Pins in Printed Circuit Board Assembly  
*Hu & Zhou, CEPREI / Guangzhou City Polytechnic*  
*Conference: IEEE ICEPT | DOI: 10.1109/ICEPT.2016.7583243*  
→ Root cause: copper sulfide (CuS, Cu2S) formation from solder paste sulfur contamination.  
→ Mechanism: electrochemical migration under bias voltage + moisture → inter-pad short.  
→ Justifies impedance monitoring as early PCB degradation indicator.

**Paper 4** — Overview of the Sulfide Corrosion Mechanism of Key Susceptible Metal Materials in Typical Electronic Components  
*Zhang, Wang, He et al., CEPREI, 2024*  
*Conference: ICEPT 2024 | DOI: 10.1109/ICEPT63120.2024.10668595*  
→ Silver and copper corrosion rates increase exponentially with humidity (power law relationship).  
→ At 80% RH, copper corrosion rate is 8× the rate at 30% RH.  
→ Justifies SHT40 humidity monitoring as a corrosion risk factor in our pipeline.

---

## Layer 4 — Failure Physics (IC / ASIC)

**Paper 2** — Failure Analysis of ASIC Controller Integrated in Embedded Flash Memory Package under Biased-HAST  
*Gan, Loke, Tan et al., Western Digital, 2024*  
*Conference: IEEE IPFA 2024 | DOI: 10.1109/IPFA61654.2024.10691167*  
→ Electrical overstress (EOS) identified as primary ASIC failure mode under accelerated testing.  
→ Lock-in thermography (LIT) used for hotspot localization — maps to our anomaly detection approach.  
→ Power dip events trigger current surges → Joule heating → metal melting.  
→ Justifies INA226 current/voltage ripple monitoring as EOS early warning signal.

**Paper 5** — Common Failure Analysis Methods and Typical Failure Mechanisms of Integrated Circuits  
*Wang & Su, CEPREI, 2022*  
*Conference: ICEPT 2022 | DOI: 10.1109/ICEPT56209.2022.9873385*  
→ Comprehensive taxonomy: EOS, ESD, electromigration, latch-up, packaging failures.  
→ Establishes SEM/EDS, X-ray, and C-SAM as standard failure analysis methods.  
→ Provides failure mode library used to build Layer 4 probable cause mapping.

---

## Edge IoT Architecture Reference

**Paper 10** — Edge-Based AI for Real-Time Threat Detection in 5G-IoT Networks: A Comparative and Architectural Review  
*Sousa, Correia & Reis, UTAD Portugal, 2025*  
*Conference: ICSC 2025 | DOI: 10.1109/ICSC65596.2025.11140446*  
→ Validates edge-first architecture for resource-constrained IoT devices.  
→ Lightweight CNN achieves 92.4% accuracy within 2 MB memory — supports our < 0.02 MB target.  
→ Federated learning framework for privacy-preserving multi-device deployment.  
→ Confirms hybrid edge-cloud approach reduces bandwidth while maintaining detection accuracy.
