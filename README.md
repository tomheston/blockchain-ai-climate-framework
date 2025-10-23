# blockchain-ai-climate-framework
code and data 
   "<a href=\"https://colab.research.google.com/github/tomheston/blockchain-ai-climate-framework/blob/main/notebooks/noaa_validation_analysis.ipynb\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"


     # Blockchain-AI Climate Data Framework: Real-World Validation

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)

Supporting code and data for: **"The Blockchain–AI Framework for Transparent Climate Data Management: A Methodological Proposal"**

## Contents

- `noaa_validation_analysis.ipynb` - Google Colab notebook implementing statistical anomaly detection
- `noaa_984290_2024.txt` - NOAA ISD hourly temperature data (Manila, Philippines, Jan-Oct 2024)
- `README.md` - This file

## Quick Start

### Run in Google Colab

1. Click here: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/tomheston/blockchain-ai-climate-framework/blob/main/notebooks/noaa_validation_analysis.ipynb)
2. Upload `noaa_984290_2024.txt` when prompted
3. Run all cells
4. Results export as `anomalies.csv`

### Run Locally

```bash
# Clone repository
git clone https://github.com/[YOUR-USERNAME]/blockchain-ai-climate-framework.git
cd blockchain-ai-climate-framework

# Open notebook in Jupyter
jupyter notebook noaa_validation_analysis.ipynb
```

**Requirements:** Python 3.7+, pandas, numpy

## Method

Validates statistical anomaly detection using z-score threshold (|z| > 3.0) on real-world climate observations.

**Algorithm:**
1. Load hourly temperature data
2. Calculate rolling 30-day baseline (mean, standard deviation)
3. Compute z-scores for each observation
4. Flag anomalies where |z| > 3.0
5. Report detected events with timestamps and magnitudes

## Data Source

**NOAA Integrated Surface Database (ISD)**
- Station: 984290-99999 (Manila Ninoy Aquino International Airport)
- Location: 14.5°N, 121.0°E
- Period: January 1 - October 31, 2024
- Records: 7,248 hourly observations
- Source: https://www.ncei.noaa.gov/data/global-hourly/

NOAA data is public domain (U.S. government work).

## Results

**34 temperature anomalies detected** (|z| > 3.0)
- Concentrated in April-May 2024 (Manila hot season)
- Temperature range: 36.9-38.0°C
- Clustered 05:00-08:00 UTC (1pm-4pm local afternoon peaks)
- Consistent with documented heat wave events

See full results in published paper.

## Citation

If you use this code or data, please cite:

```
Heston TF. The Blockchain–AI Framework for Transparent Climate Data 
Management: A Methodological Proposal. PLOS Climate. 2025. [In press]
```

## License

- **Code:** MIT License - Free to use, modify, distribute
- **Data:** Public domain (NOAA) / CC-BY-4.0 (derivatives)
- **Documentation:** CC-BY-4.0

## Reproducibility

All analysis is fully reproducible:
- Fixed random seed (where applicable)
- Standard statistical methods (NumPy/Pandas)
- No proprietary software required
- Complete parameter documentation in paper

Expected runtime: 2-5 minutes

## Contact

**Tom Heston, MD**  
Washington State University  
Email: tom.heston@wsu.edu  
ORCID: [0000-0002-5655-2512](https://orcid.org/0000-0002-5655-2512)

## Acknowledgments

NOAA National Centers for Environmental Information for providing open climate data.

---

**Repository archived on Zenodo:** https://doi.org/10.5281/zenodo.XXXXXXX

**Last updated:** 2025-10-23
