# smart-traffic-control-system
An Arduino-based smart traffic controller featuring density-based adaptive signal timing, emergency vehicle prioritization, and pedestrian request handling, simulated using Wokwi.

Problem Statment:

A smart-city junction controller reads four inductive-loop density sensors (0–255 vehicles/hour count),
four pedestrian push-button stations and ambulance/fire priority transponders; it drives twelve lamps and
reports statistics on a serial link. Given data: density update 2 s; green 15–90 s; yellow 3 s; all-red 2 s;
emergency pre-emption ≤ 500 ms; pedestrian service ≤ 120 s; reporting every 60 s at 9600 bps; RAM 256
B; ROM 8 KB; CPU utilisation ≤ 30%; one sensor may fail permanently; throughput target ≥ 800
vehicles/hour.
Design the firmware architecture and prove — by interrupt-latency calculation, timer allocation, memory
budgeting, scheduling analysis and simulated congestion scenarios — that emergency response,
throughput, fairness, communication and fault tolerance all hold. Improving one objective degrades
another: the trade-off must be engineered, not assumed
(c - constraints)

C1 --- Emergency pre-emption within 500 ms 

C2 --- CPU utilisation ≤ 30% 

C3 --- Junction throughput ≥ 800 vehicles/hour while any lane wait ≤
120 s


C4 --- Continued operation after one permanent sensor failure 

C5 --- Memory ≤ 8 KB ROM / 256 B RAM; statistics transmitted every
60 s at 9600 bps
