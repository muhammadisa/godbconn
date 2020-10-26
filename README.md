<h1 align="center">Welcome to godbconn 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-1.0.0-blue.svg?cacheSeconds=2592000" />
  <img alt="documentation: yes" src="https://img.shields.io/badge/Documentation-Yes-green.svg" />
  <img alt="maintained: yes" src="https://img.shields.io/badge/Maintained-Yes-green.svg" />
</p>



>This package is pretty simple, just for connect to data base using Go SQL standard library which support 3 kinds Popular database, MySQL, Postgres and Microsoft SQL.



### Simple & Complete usage

For MySQL

```go
err := godotenv.Load()
if err != nil {
    log.Fatal(err)
}
// Load database credential env and use it
db, err := godbconn.DBCred{
    DBDriver:   "mysql",
    DBHost:     os.Getenv("DB_HOST"),
    DBPort:     os.Getenv("DB_PORT"),
    DBUser:     os.Getenv("DB_USER"),
    DBPassword: os.Getenv("DB_PASSWORD"),
    DBName:     os.Getenv("DB_NAME"),
}.Connect()
if err != nil {
    log.Fatal(err)
}
```

For Postgres

```go
err := godotenv.Load()
if err != nil {
    log.Fatal(err)
}
// Load database credential env and use it
db, err := godbconn.DBCred{
    DBDriver:   "postgres",
    DBHost:     os.Getenv("DB_HOST"),
    DBPort:     os.Getenv("DB_PORT"),
    DBUser:     os.Getenv("DB_USER"),
    DBPassword: os.Getenv("DB_PASSWORD"),
    DBName:     os.Getenv("DB_NAME"),
}.Connect()
if err != nil {
    log.Fatal(err)
}
```

For MsSQL

```go
err := godotenv.Load()
if err != nil {
    log.Fatal(err)
}
// Load database credential env and use it
db, err := godbconn.DBCred{
    DBDriver:   "mssql",
    DBHost:     os.Getenv("DB_HOST"),
    DBPort:     os.Getenv("DB_PORT"),
    DBUser:     os.Getenv("DB_USER"),
    DBPassword: os.Getenv("DB_PASSWORD"),
    DBName:     os.Getenv("DB_NAME"),
}.Connect()
if err != nil {
    log.Fatal(err)
}
```



