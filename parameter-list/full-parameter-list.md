---
layout: default
title: Full Parameter List
parent: Parameter List
nav_order: 1
---

# Full Parameter List

## List of all the cli parameters in EmuFlight 1.0.0 (still a work in progress)

| Parameter Name | Description | Min/Max/Table | Default | Units |
|----------------|-------------|---------------|---------|-------|
| gyro_hardware_lpf | Filter that the gyro hardware produces. Normal is suggested. | NORMAL, EXPERIMENTAL | NORMAL | |
| gyro_high_range | Increases the max DPS that your gyro can read. Only works for some gyros. (list those later) | ON, OFF | OFF |  |
| gyro_lowpass_type | Filter order for the gyro lowpass filter. Higher orders have sharper cutoff. | PT1, PT2, PT3, PT4 | PT1 | |
| gyro_notch1_hz | Center frequency for a notch filter placed on the gyro. A value of 0 disables the filter. | 0-4000 | 0 | Hz |
| gyro_notch1_cutoff | Cutoff frequency for the gyro notch filter. | 0-4000 | 0 | Hz |
| gyro_abg_alpha | Alpha value for a Alpha Beta Gamma filter on the gyro. Alpha Beta Gamma filters are simplified forms of observer for estimation, data smoothing and control applications. Higher values are less filtering and lower values filter more. When set to low the data lags, but to high and it doesn't do a whole lot of filtering. | 0-1000 | 0 |  |
| gyro_abg_boost | A non-linear boost to the error which the Alpha Beta Gamma filter uses in its calculations. Higher boost will make the Alpha Beta Gamma filter more responsive, but a bit noisier. | 0-2000 | 375 |  |
| gyro_abg_half_life | Reduces the scope of data which the Alpha Beta Gamma filter uses to make its prediction. The default of 50 means that after half a second the Alpha Beta Gamma remembers only half of the history. This makes the Alpha Beta Gamma filter rely more on newer data rather than old data. | 0-1000 | 50 | Seconds/100 |
| gyro_calib_duration | The amount of time used for gyro calibration. | 50-3000 | 125 | Seconds/100 |
| gyro_calib_noise_limit | Noise level the gyro must be below during the gyro calibration | 0-200 | 48 |  |
| gyro_offset_yaw | Meant to deal with yaw attitude drift. Only works when board are aligned normally and not exotically. The basic setup can be done on the bench without LiPo, USB powered power on, do not move the quad for 10 minutes for CW set a positive value equal to the drift, and negative for the CCW direction. | -1000-1000 | 0 |  |
| imuf_roll_q | Trust value for the kalman filter on the roll axis. (need to finish this) | 0-16000 | 3200 |  |
| imuf_pitch_q | Trust value for the kalman filter on the pitch axis. (need to finish this) | 0-16000 | 3200 |  |
| imuf_yaw_q | Trust value for the kalman filter on the yaw axis. (need to finish this) | 0-16000 | 3200 |  |
| imuf_w | Number of samples the kalman filter looks at for its prediction. Larger drones generally fly better with higher w values. | 0-300 | 32 |  |
| gyro_overflow_detect |  | OFF, YAW, ALL | ALL |  |
| yaw_spin_recovery |  | OFF, ON, AUTO | AUTO |  |
| yaw_spin_threshold |  | 500-1950 | 1950 | deg/sec |
| gyro_use_32khz |  | OFF, 16K, 32K | OFF |  |
| gyro_to_use |  | FIRST, SECOND, BOTH | FIRST |  |
| leaving space for dyn notch stuff |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
| dyn_lpf_gyro_min_hz |  | 0-1000 | 115 | hz |
| dyn_lpf_gyro_width |  | 0-255 | 0 | % |
| dyn_lpf_gyro_curve_expo |  | 0-10 | 5 |  |
| dyn_lpf_gain |  | 0-200 | 0 |  |
| gyro_filter_debug_axis |  | ROLL, PITCH, YAW | ROLL |  |
| smith_predict_str |  | 0-100 | 50 |  |
| smith_predict_delay |  | 0-80 | 40 | ms/10 |
| smith_predict_filt_hz |  | 0-10000 | 5 | Hz |
| acc_hardware |  |  |  |  |
| acc_high_range |  |  |  |  |
| acc_lpf_hz |  | 0-400 |  | Hz |
| acc_trim_pitch |  | -300-300 | 0 |  |
| acc_trim_roll |  | -300-300 | 0 |  |
| acc_calibration |  |  |  |  |
| align_mag |  |  |  |  |
| mag_align_roll |  | -3600-3600 | 0 | deg/10 |
| mag_align_pitch |  | -3600-3600 | 0 | deg/10 |
| mag_align_yaw |  | -3600-3600 | 0 | deg/10 |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |