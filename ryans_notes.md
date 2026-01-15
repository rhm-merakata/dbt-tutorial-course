# Notes

## Generating a model (e.g., stg_ecommerce__orders.sql) from a model source file (e.g., src_ecommerce.yml)

Note that `the macro macro_generate_base_table.sql` is required for this to work.

```bash
dbt run-operation generate_base_model --args '{"source_name": "thelook_ecommerce", "table_name": "orders"}'
```

## Generating a yaml (e.g., stg_ecommerce__orders.yml) from a model (e.g., stg_ecommerce__orders.sql)

```bash
dbt run-operation generate_model_yaml --args '{"model_names": ["stg_ecommerce__orders"]}'
```
