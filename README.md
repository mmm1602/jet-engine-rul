
# Jet Engine RUL Prediction

Predicting turbofan engine **Remaining Useful Life (RUL)** using multiple linear regression.

## Dataset

NASA C-MAPSS FD001 — simulated high-pressure compressor degradation.

- `train_FD001.txt` 100 training engines
- `test_FD001.txt` 100 test engines
- `RUL_FD001.txt` Test RUL values

## Setup

Requires Python 3.12.

```bash
git clone https://github.com/mmm1602/jet-engine-rul.git
cd jet-engine-rul
python3 -m venv .env
source .env/bin/activate
pip install -r requirements.txt
```

Open `notebooks/analysis.ipynb` in VS Code and select the `.env` kernel.

## Methodology

Multiple linear regression:

$$
\widehat{RUL}=\beta_0+\sum_{j=1}^{p}\beta_jX_j
$$

Where \($X_j$\) represents selected engine sensor measurements.

## Project Roadmap

- [X] Load training dataset
- [X] Calculate training RUL
- [X] Analyze engine lifetime distribution
- [ ] Explore sensor statistics and correlations
- [ ] Select relevant sensors
- [ ] Fit multiple linear regression model
- [ ] Validate model and examine residuals
- [ ] Evaluate test predictions using MAE and RMSE
- [ ] Document results and conclusions

## Project Structure

```text
data/          NASA FD001 dataset
notebooks/     Python analysis
figures/       Generated plots
```
