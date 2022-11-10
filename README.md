# CYBER-SEC-GAME-BACKEND
A GraphQL API for Cyber security game.

## Tech stack
- Server language: Go 1.18.1
- Database: MySQL
- ORM: GORM
- gqlgen

## Setup
- Clone this repo
- Create .env file from .env.example
- Run ```docker-compose up```

## To generate model from the graphql schema
```bash
delete scheme.resolvers.go (if it exists)
comment all lines after User (line 65) in gqlgen.yml 
go run github.com/99designs/gqlgen@v0.17.20 generate
go run github.com/99designs/gqlgen@v0.17.20
copy paste new type/inputs from model/model_gen.go to models/models.go
uncomment all the commented code in gqlgen.yml
go run github.com/99designs/gqlgen@v0.17.20 generate
go run github.com/99designs/gqlgen@v0.17.20
```
