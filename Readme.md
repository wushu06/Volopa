# docker-compose-laravel (Volopa project)

## Usage

- `docker-compose up -d --build`.
- `docker-compose run --rm composer install`
- `docker-compose run --rm npm run dev`
- `docker-compose run --rm migrate:refresh --seed`


## Testing

```
docker-compose run --rm php ./vendor/bin/phpunit
```

## Endpoints
#### Get all tickets
``
Get /api/tickets
``

#### Create new ticket
``
Post /api/etickets
``

#### Delete ticket
``
Delete /api/ticket/[id]
``

### Search for ticket by first name or last name
``
Get /api/tickets/search/{name}
``

### Sort result 
``
Get /api/tickets/sort/{filter}
``

### Filter result
``
Post /api/tickets/filters/
``

### Extra 
Built a quick package `nour/filter` to filter result by passing any column name to the endpoint.

### xdebug

for phpstorm you will need to map the project `src` to `/var/www/html` in the server tab