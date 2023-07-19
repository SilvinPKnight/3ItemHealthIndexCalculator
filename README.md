% Title: MATLAB App Code: FRAILMatics 3-Item Health Index Calculator
%
% Version: 1.0
%
% Author: Silvin Knight, PhD
% School of Medicine
% Trinity College, The University of Dublin
%
% Acknowledgments: The authors would like to acknowledge the continued commitment
% and co-operation of the TILDA participants and research team.
%
% Funding: This research was funded by Science Foundation Ireland (SFI),
% grant number 18/FRL/6188. The Irish Longitudinal Study on Ageing
% (TILDA) is funded by Atlantic Philanthropies, the Irish Department
% of Health and Irish Life.
%
% Description: This MATLAB App calculates the FRAILMatics 3-item Health Index, which
% provides an overall measure of health status in older adults based on
% beat-to-beat blood pressure variability, cognitive function
% as assessed by the SART test, and gait speed data. The FRAILMatics
% Health Index values are normalized to a large population-level
% dataset of approximately 4300 community-dwelling individuals aged
% over 50 years from the TILDA study. The code is compatible with
% MATLAB versions R2018a and higher and can be easily integrated
% into existing MATLAB projects.
%
% License: This code is released under the terms of the GitHub. Feel free to
% use and modify the code with proper acknowledgments.
%
% Sample Entropy calculations performed using code modified from Víctor 
% Martínez-Cagigal (2018). Sample Entropy. Mathworks.
%
% Repository: https://github.com/SilvinPKnight/3ItemHealthIndexCalculator
%
% Inputs:
% - "sBP_values.csv": This file contains the systolic blood pressure (sBP) 
%   absolute values at each beat. Each row represents the data for an individual 
%   partici-pant, with the sBP values listed sequentially.
% - "sBP_timepoints.csv": This file contains the corresponding time points 
%   for each sBP beat (in ms). It enables the synchronization of the sBP values 
%   with the respective time intervals. Similar to the previous file, each row 
%   corresponds to a participant, and the time point values are listed sequentially.
% - "SART_data.csv": This file contains the SART (Sustained Attention Reaction 
%   Time) data. Each row represents a participant, and the columns represent the 
%   reaction time values in milliseconds (ms). The data is orga-nized in a tabular
%   format, facilitating straightforward data loading and pro-cessing.
% - "gait_speed.csv": This file contains the usual gait speed data. It is structured 
%   as a single column vector, where each value represents the gait speed in centimeters 
%   per second (cm/s) for an individual participant.
% NOTE: The naming of data files does not matter to the processing.
%
% Outputs:
% - FRAILMatics_HI: FRAILMatics Health Index values normalized to the TILDA
% dataset, as well as Risk Groups (0: Low; 1: Medium; 2: High)
%
% Contact: silvin.knight@tcd.ie
%
% Last Updated: June 19, 2023
