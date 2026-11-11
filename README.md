# estudio_mascotas_ipc_grupo_15

Study of the genetic and clinical data of the pets belonging to the members of IPC Group 15.

## Repository structure

```
estudio_mascotas_ipc_grupo_15/
├── pets_data/
│   └── <github_user>/
│       ├── cats.csv
│       ├── dogs.csv
│       └── genes/
│           └── <Class>_<Name>.fasta
├── scripts/
│   ├── python/
│   └── r/
├── LICENSE
└── README.md
```

### `pets_data/`

One folder per group member, named after their GitHub user.

- **Clinical data:** one CSV per animal class (`cats.csv`, `dogs.csv`, ...), `;` separated, with the columns `name`, `age`, `weight`, `race`, `cause_of_death`.
- **Genetic data:** FASTA files in `genes/`, named `<Class>_<Name>.fasta` (e.g. `Cat_Coqueta.fasta`).

### `scripts/`

Python and R scripts that use the data in `pets_data/`.

| Script | Description | Input |
|---|---|---|
| `python/pets_by_owner.py` | Lists all pets associated with an owner | `user` (GitHub user) |
| `r/cause_of_death_summary.R` | Summarizes pets per class/owner, causes of death and mean age/weight by class | None |

## Requirements

- Python 3
- R

## Usage

Run the scripts from the repository root:

```bash
python scripts/python/pets_by_owner.py <user>
Rscript scripts/r/cause_of_death_summary.R
```

## Authors

Made, Maria Paula, Marco and Martin – IPC Group 15

## License

See [LICENSE](LICENSE).
