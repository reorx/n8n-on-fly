# n8n on fly


## How to setup

1. Fork the repo
2. Customize `fly.toml` and `prod.env` to suit your own needs.
3. Run the following commands:

    ```bash
    fly deploy
    fly secrets import < prod.env
    ```

## Caveats

### `prod.env`

`prod.env` should contain the following env vars:

```
DB_POSTGRESDB_HOST=db.***.supabase.co
DB_POSTGRESDB_PASSWORD=*****
N8N_ENCRYPTION_KEY=*****
```

Note that you MUST NOT add double quotes around the env values due to [this issue](https://github.com/superfly/flyctl/issues/589)
