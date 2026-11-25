# AirBreak Mumbai

AirBreak Mumbai is a school-planning interface prototype for choosing when to schedule outdoor activities. We designed a workflow that lets teachers and timetable planners compare feasible times against an hourly forecast of fine-particle pollution (PM2.5), while accounting for class timetables, lunch breaks, and shared playground capacity.

The project was inspired by the **2026 Google Mumbai Data Challenge: Air Quality Mapping & Forecasting**, run by Google on Zindi with Beyond as programme partner. The challenge asked participants to forecast hourly PM2.5 at Mumbai monitoring stations. AirBreak explored how a school might use that kind of forecast to make a timetable decision. [Official challenge](https://zindi.world/competitions/google-mumbai-data-challenge) · [Challenge launch](https://luma.com/h3hq02qb)

## How the prototype works

1. **Set the school day.** Enter school hours, breaks, and how many groups the outdoor space can accommodate.
2. **Describe the sessions.** Specify which classes need outdoor time and how long each session should last.
3. **Compare feasible times.** Review the windows that fit the timetable and available space alongside an illustrative hourly PM2.5 chart.

For example, suppose two classes need the same playground and the chart shows its lowest estimated PM2.5 during lunch. The lunch break rules out that window. The teacher can compare the remaining windows and consider staggering the sessions if capacity only allows one class at a time.

## Design choices and validation scope

- **Start with the timetable.** A lower estimated pollution level is only useful if a full session fits and the playground is available. Putting those constraints first makes the options easier to compare.
- **Account for forecast uncertainty.** When two feasible windows have similar estimates, a small difference on the chart may offer little basis for preferring one. The walkthrough uses illustrative values. Estimating how often those differences are meaningful would require comparing forecasts with later observations.
- **Evaluate forecasting and school use separately.** The separate challenge entry covered data processing, time-based validation, and model evaluation. The challenge scored forecasts by root mean squared error (RMSE), where lower is better. AirBreak demonstrates the planning interaction. Live data integration, operational school use, and effects on scheduling or exposure remain unverified. [Challenge evaluation](https://zindi.world/competitions/google-mumbai-data-challenge)

## Repository contents

[`README.md`](README.md) is the complete repository and serves as the prototype walkthrough. The case study can be read directly on GitHub.
