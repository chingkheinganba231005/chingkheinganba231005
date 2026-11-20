# Chingkheinganba Rajkumar

**BEng (Artificial Intelligence and Data Science) · The University of Hong Kong · Class of 2029**  
Minor in Astronomy (intended)

I build machine learning for real problems: computer vision for low-resource scripts and industrial inspection, causal inference for business decisions, surrogate modelling and scientific ML, and machine learning on real astronomical and market data. I care about honest evaluation: held-out tests touched once, confidence intervals, and strong simple baselines.

## Research

Two sole-author papers on handwritten Meitei Mayek, the script of Manipuri:

**[Beyond Isolated Characters: The First Segmentation-Free Recogniser of Handwritten Meitei Mayek Words](https://github.com/chingkheinganba231005/meitei-mayek-word-recognition)**  
*Under peer review at The Visual Computer (Springer Nature) · [Preprint on Research Square](https://www.researchsquare.com/article/rs-11184324/latest) · [Live demo](https://huggingface.co/spaces/Chingkheinganba/handwritten-meitei-mayek-word-recognition)*  
The first recogniser that reads whole handwritten Meitei Mayek words without segmenting them into characters. With no transcribed handwritten words available, I composed training words from isolated characters and trained a ConvNeXt–BiLSTM–CTC model with a character language model. **2.96% character error rate** on a small real-handwriting test set of 100 words from one writer, released publicly.

**[Pretrained Eyes on an Old Script: New State of the Art in Handwritten Meitei Mayek Recognition](https://github.com/chingkheinganba231005/Handwritten-Meitei-Mayek-Recognition)**  
*Under review at Scientific Reports (Springer Nature) · [Live demo](https://huggingface.co/spaces/Chingkheinganba/handwritten-meitei-mayek-recognition)*  
Fine-tuned and ensembled six ImageNet-pretrained CNNs for 55-class handwritten character recognition. **New state of the art: 98.12% accuracy** on the official TUMMHCD test set, up from 97.08% (35% fewer errors), with ablations, error analysis and reproducible experiments.

## Applied machine learning

**[Visual defect detection for product inspection](https://github.com/chingkheinganba231005/Visual-defect-detection)**  
PatchCore anomaly detection on all 15 MVTec AD product categories, trained only on photos of good parts. Mean image AUROC **0.987** (95% CI 0.983–0.992) against 0.868 for a Gaussian baseline, with heatmaps that locate the defect. Used for inspection triage it avoids **79% of manual checks** at a 2% defect rate, and it runs as a FastAPI service in Docker at 71 ms per image on a CPU.

**[Uplift modelling on the Criteo ad trial](https://github.com/chingkheinganba231005/Uplift-modelling)**  
Who should see an ad? Five uplift models compared on a 14-million-user randomised trial, with the data explored in SQL (DuckDB). The randomisation check found the trial pools several tests, and a doubly robust (AIPW) estimate showed the naive effect was 13% too high. When ads are expensive, a causal-forest targeting rule earns **$30k per million users** where showing the ad to everyone loses $2.8k.

**[How reliable are Hong Kong's bus arrival times?](https://github.com/chingkheinganba231005/Predicting-HK-bus-delays)** *(collecting data)*  
A collector polls the KMB and Citybus real-time APIs every minute for 11 routes, together with Hong Kong Observatory weather. The APIs give only predictions, so I infer when each bus actually arrived from the stream of predictions (99% of bus tracks resolved on a real sample). Quantile models with conformal ranges, and a live dashboard. Results come after a few weeks of collection.

## Project collections

**[Surrogate modelling and scientific ML](https://github.com/chingkheinganba231005/Surrogate-modelling-projects)**: six end-to-end projects  
Gaussian-process surrogate and constrained Bayesian optimisation for heat-sink design (0.23% test error) · Fourier neural operator from scratch (0.44% test error, ~170× faster than the solver) · low-carbon concrete with conformal bounds (test R² 0.90) · physics-informed neural networks on real soil-temperature data · climate-model emulation · epidemic-model calibration with emulators (35× fewer simulator runs).

**[Quantitative finance](https://github.com/chingkheinganba231005/Quant-Fintech-projects)**: eight projects on real market data  
Volatility forecasting with GARCH fitted from scratch, where HAR with the VIX was best of nine models and volatility targeting cut max drawdown from −55% to −39% · Heston model calibrated to the SPY option chain (0.58 vol points) with a neural pricer ~100× faster · portfolio construction over a 50-year walk-forward · factor investing with ML ranking · pairs trading · optimal execution and market making · a pre-registered regime-switching strategy that honestly failed its Sharpe test.

**[Machine learning for astrophysics](https://github.com/chingkheinganba231005/Astronomy-ML-projects)**: six projects on real observational data  
Exoplanet detection in NASA Kepler data (test ROC AUC 0.97; 7 of Kepler-90's 8 planets recovered) · cosmological parameters from 1,701 supernovae · mass of the Milky Way's black hole (≈4.5 million solar masses) · rediscovering Neptune and Kepler's laws · the timing of the ice ages.

**[C++ systems and performance](https://github.com/chingkheinganba231005/Cpp-projects)**: seven projects in modern C++  
Autograd machine-learning library from scratch · matrix multiplication ~25× faster than the naive version (SIMD, cache blocking, threads) · low-latency order-matching engine · lock-free queue (328M messages/s) · custom memory allocators · entity-component system · 3D software rasteriser.

## Other projects

- **[Trees vs Breath](https://github.com/chingkheinganba231005/Trees-vs-breathe)**: Physics-informed decision-support prototype for studying how street trees affect heat and pedestrian exposure to air pollution. I led the team to the **top 8 at HacKU 2026**.
- **[Reading by Redrawing](https://github.com/chingkheinganba231005/Meitei-Mayek-Redraw)**: Handwritten character recognition with differentiable Bézier-stroke reconstruction and controlled gradient routing.
- **[TailSafe](https://github.com/chingkheinganba231005/Tail_Safe)**: Monte Carlo evacuation stress testing with risk metrics, counterfactual analysis and a graph-neural-network surrogate. *Simulation research prototype, not a certified safety assessment.*

## Open source contributions

**[scikit-learn](https://github.com/scikit-learn/scikit-learn)**  
- [#35200](https://github.com/scikit-learn/scikit-learn/pull/35200): clearer "empty vocabulary" error in `CountVectorizer` and `TfidfVectorizer` when `ngram_range` is the cause (issue #33981), with regression tests.  
- [#35202](https://github.com/scikit-learn/scikit-learn/pull/35202): user-guide documentation on when to use the Calinski–Harabasz score instead of the Silhouette Coefficient (issue #8647), with every claim checked by experiment.

## Honours

- HacKU 2026: Top 8 Finalist, team leader (Oct 2026)
- HKU Undergraduate Entrance Scholarship for Outstanding Academic Talents (Sep 2025)
- Pi-Summit 2024: First Prize, national inter-school mathematics competition (Sep 2024)

## Tools

**Languages:** Python, C++ (C++23), SQL, JavaScript  
**ML and data:** PyTorch, scikit-learn, LightGBM, econml, NumPy, pandas, SciPy, statsmodels, DuckDB, Matplotlib, Astropy  
**Engineering:** Git/GitHub, GitHub Actions, pytest, FastAPI, Docker, Streamlit, Jupyter, CMake

## Contact

[LinkedIn](https://www.linkedin.com/in/chingkheinganba-raj-kumar-3787543b4) · [Email](mailto:chingkheinganbaofficial@gmail.com) · [ORCID](https://orcid.org/0009-0002-2620-0281)
