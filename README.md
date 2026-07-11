# AstroShield

AI-powered satellite conjunction risk assessment system that predicts collision probability and recommends avoidance maneuvers for CubeSats in low Earth orbit.

## The Problem

Low Earth orbit is increasingly congested, with thousands of active satellites and tens of thousands of debris fragments on intersecting trajectories. CubeSats lack the onboard processing and operator bandwidth to assess conjunction risk in real time. Without automated guidance, a satellite operator may not respond to a close approach until it is too late to execute a safe avoidance burn.

## My Solution

AstroShield uses a logistic regression model trained on real conjunction warning data (miss distance, relative velocity, time to closest approach, nearby object count, and counter-orbit flag) to score each conjunction event as it develops. When risk exceeds a threshold, the system selects a maneuver method (prograde, retrograde, radial, or plane-change burn) and computes the required ΔV. The approach is validated through an interactive simulation that replays real warning events from the dataset and shows the satellite's response with and without AI guidance active.

## Results

The model correctly identifies high-risk conjunctions across all 12 real warning events in the dataset. With AI guidance enabled, the satellite executes targeted avoidance burns and clears every conjunction with positive miss-distance margin. With guidance disabled, conjunctions with miss distances below 0.12 km result in logged impacts, demonstrating the cost of no automated response.

## Repository Structure

- `/code` — Notebooks and scripts (Python)
- `/docs` — Research paper and pitch deck
- `/data` — Dataset references
- `/results` — Charts and output files

## Dataset

**Real CubeSat Conjunction Dataset** — derived from historical Space-Track conjunction data messages (CDMs) for CubeSats in LEO. Includes conjunction warning events with miss distance, relative velocity, TCA, nearby object count, altitude, and counter-orbit flag.

Source: [space-track.org](https://www.space-track.org)

## Project Website

[your-project-website-url]

## Contact

[Your Name] — [your@email.com]
