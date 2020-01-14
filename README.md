# Suministros Puerto Rico

https://suministrospr.com

## Development

```bash
$ cp example.env .env
$ pipenv install --dev
$ pipenv run python manage.py migrate
$ pipenv run python manage.py runserver_plus
```

### Docker

```bash
$ docker-compose up --build
```

#### Importing data

1. Unarchive [data extract](https://github.com/Code4PuertoRico/suministrospr/issues/8#issuecomment-573977666) to `./data/scraped/*.json`

2. Run the import_data command:

  ```bash
  $ docker-compose exec web python manage.py import_data ./data/scraped
  ```
