# Simple sample dbt project with DuckDB

## Prepare

```
python -m venv venv
source venv/bin/activate
pip install -r sandbox/requirements.lock

cd sandbox
```

## Run dbt command
Run
```
dbt run --profiles-dir "$(pwd)/profiles/"
```

Check tables

```
> duckdb dev.duckdb -c '.tables'
my_first_dbt_model   my_second_dbt_model
> duckdb dev.duckdb -c 'select * from my_second_dbt_model'
┌───────┐
│  id   │
│ int32 │
├───────┤
│     1 │
└───────┘
```


