# 🧪 Data Playground

A collection of curated and synthetic datasets for ML research, evaluation, and benchmarking — with a focus on LLM capabilities and alignment.

## Datasets

| Dataset | Domain | Rows | Task | Status |
|---------|--------|------|------|--------|
| [Instruction Following Eval](./datasets/instruction-following-eval/) | NLP / LLM Evaluation | 50 | Constraint compliance detection | ✅ Released |

## Structure

```
data-playground/
├── datasets/
│   └── instruction-following-eval/
│       ├── README.md              # Dataset card
│       ├── data.csv               # Raw dataset
│       └── schema.json            # Column definitions
├── scripts/
│   ├── validate.py                # Schema validation
│   └── stats.py                   # Dataset statistics
├── LICENSE
└── README.md
```

## Quick Start

```bash
# Clone the repo
git clone https://github.com/<your-username>/data-playground.git
cd data-playground

# Load a dataset
python -c "
import pandas as pd
df = pd.read_csv('datasets/instruction-following-eval/data.csv')
print(df.shape)
print(df['difficulty'].value_counts())
"
```

## Contributing

New datasets are welcome. Each dataset should include:
- A `README.md` dataset card following the template in `datasets/`
- Raw data files in `.csv`, `.json`, or `.parquet` format
- A `schema.json` describing columns and types

## License

This project is licensed under the Apache 2.0 License — see [LICENSE](./LICENSE) for details.

Individual datasets may carry their own licenses as noted in their respective README files.
