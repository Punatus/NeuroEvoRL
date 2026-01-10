# NeuroEvoRL

Kleines Arbeits-Repository mit Prototypen zur automatischen Architektur- und
Hyperparameter-Optimierung für Reinforcement-Learning-Agenten. Dieses Repo
enthält vor allem Jupyter-Notebooks mit Trainings- und Prototyp-Code.

## Enthaltene Dateien
- `LL-Train-Single.ipynb` — DQN-Training (LunarLander-v2) mit dynamischem MLP,
  Replay-Buffer und Checkpoint-/Video-Utilities.
- `ll09-01-cartpole.ipynb` — CartPole-Experimente / Beispiel-Notebook.
- `lunarlander_base_prototype.ipynb` — REINFORCE-Policy-Gradient-Prototyp für
  LunarLander-v3 als Basis für evolutionäre Erweiterungen.

## Kurz: Ziele & Status
- Prototypische Implementierungen (Notebooks) zum schnellen Experimentieren.
- Fokus auf `LunarLander-v3` und `CartPole` als Benchmarks.
- Ergebnisse (Modelle / Checkpoints) werden in `training_history/` abgelegt.
  Videos werden in `videos/` gespeichert, wenn die Recording-Funktionen genutzt werden.

## Voraussetzungen
- Python 3.9+ (Windows / Linux / macOS)
- Empfohlene Pakete (minimal): `torch`, `gymnasium`, `numpy`, `matplotlib`

Schnellinstallation (z. B. in einer venv):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1    # Powershell
pip install --upgrade pip
pip install torch gymnasium numpy matplotlib
```

Hinweis: Einige Notebooks verwenden `gymnasium[box2d]` oder `RecordVideo`.
Installiere zusätzliche Extras bei Bedarf.

## Schnellstart
- Öffne eines der Notebooks in VS Code / Jupyter Notebook / JupyterLab / Kaggle Notebook.
- `LL-Train-Single.ipynb` enthält einen vollständigen Trainingsloop, Logging
  (CSV) und Funktionen zum Speichern von Modell-Bundles (`training_history/`).
- `lunarlander_base_prototype.ipynb` eignet sich als kompakte Basis für
  Policy-Gradient-Experimente.

## Hinweise zur Reproduktion
- Viele Notebooks setzen Seeds und schreiben Checkpoints in `training_history/`.
- Videos werden in `videos/` erstellt, wenn `run_trained_model_and_record()`
  oder Notebook-Zellen mit `RecordVideo` verwendet werden.