# Dataset-for-onboard-aeroengine-gas-path-diagnosis
This repository contains the datasets involved in the paper titled "Towards domain shifts: Stream fine-tuning via feed-forward fault data generation for on-board aero-engine gas-path diagnosis".

Download Link: https://cloud.189.cn/t/2MfmAjqEN3M3

Password：kv4b

Unzipped Password: xjtuftc

===================== Case Setting =====================

Table 1 provides a summary of three simulated datasets. 

Dataset 1 is utilized for method development, while the other two are used for testing. 

These datasets are generated through the onboard engine model with the introduction of various uncertainty factors and fault modes. 

Table 1. Settings of the Simulated Datasets.

| Element                     | Dataset 1      | Dataset 2      | Dataset 3           |
|-----------------------------|----------------|----------------|---------------------|
| Engine individual           | None           | A              | B                   |
| Flight num                  | 36             | 36             | 40                  |
| Flight profile              | 4              | 4              | 10                  |
| Sea-surface temperature     | Random,-15~30℃ | Random,-15~30℃ | Random,-15~30℃      |
| Performance deterioration/K | 0,10,20,30     | 0,8,16,25      | Continuous changing |
| Sensor noise and bias       | Random         | Random         | Random              |
| Sensor drift                | None           | None           | Continuous changing |
| Fault Mode                  | Table 2        | Table 2        | Table 3             |
 
 
Table 2. Fault Modes in Dataset 1 and 2.

| No. | Component | Efficiency | Flow capacity |
|-----|-----------|------------|---------------|
| 1   | Fan       | -2.33%     | -0.93%        |
| 2   | Fan       | -2.24%     | -1.34%        |
| 3   | HPC       | -2.69%     | -1.08%        |
| 4   | HPC       | -2.68%     | -1.61%        |
| 5   | HPT       | -1.85%     | +0.74%        |
| 6   | HPT       | -1.78%     | +1.07%        |
| 7   | LPT       | -2.77%     | +1.11%        |
| 8   | LPT       | -2.66%     | +1.60%        |

Table 3. Fault Modes in Dataset 3.

| No. | Component | Efficiency | Flow capacity |
|-----|-----------|------------|---------------|
| 1   | Fan       | -2.40%     | -1.00%        |
| 2   | HPC       | -2.70%     | -1.70%        |
| 3   | HPT       | -1.40%     | +2.80%        |
| 4   | LPT       | -2.40%     | +3.10%        |

===================== File Rule =====================

TXT file naming rules: 

Dataset 1 and 2:  fault mode code + Performance deterioration

Dataset 3: FB + flight number (+_label)

Label: 0: Fault-Free; 1: Fan Fault; 2: HPC Fault; 3: HPT Fault; 4: LPT Fault.

The Data in the TXT file are arranged in columns in the following order:
| No. | Header                            |
|-----|-----------------------------------|
| 1   | Run time                          |
| 2   | Fan Speed 1                       |
| 3   | Fan Speed 2                       |
| 4   | HPC Speed 1                       |
| 5   | HPC Speed 2                       |
| 6   | Inlet Total Temperature           |
| 7   | Inlet Total Pressure              |
| 8   | Inlet Static Pressure             |
| 9   | Fan Exit Duct Total Temperature 1 |
| 10  | Fan Exit Duct Total Temperature 2 |
| 11  | Fan Exit Duct Total Pressure 1    |
| 12  | Fan Exit Duct Total Pressure 2    |
| 13  | HPC Exit Total Temperature 1      |
| 14  | HPC Exit Total Temperature 2      |
| 15  | HPC Exit Static Pressure 1        |
| 16  | HPC Exit Static Pressure 2        |
| 17  | Fuel Mass Flow of Main Combustor  |
| 18  | LPT Exit Total Temperature 1      |
| 19  | LPT Exit Total Temperature 2      |
| 20  | LPT Exit Total Pressure 1         |
| 21  | LPT Exit Total Pressure 2         |

where, XX 1 is the measured value of the sensors, XX 2 is the output value of the airborne model, and other parameters without 1 or 2 are the measured value of the sensors.

===================== Detailed Information =====================

For more details about the simulation, see:

Liao Z, Wang J, Liu J, et al. Uncertainties in gas-path diagnosis of gas turbines: Representation and impact analysis. Aerospace Science and Technology, 2021,113:106724.

Your comments and citation are welcome!
