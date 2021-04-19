# Simple txAdmin recipe
## Requirements
### Create database user:
```sql
> CREATE USER 'upg'@'localhost' IDENTIFIED VIA|WITH mysql_native_password BY '{{password}}';
> GRANT ALL privileges ON `{{dbName}}`.* TO 'upg'@'localhost';
> FLUSH PRIVILEGES;
```
#### Verify permissions
```sql
> SHOW GRANTS FOR 'upg'@'localhost';
```

> The database will be created automatically by txAdmin using the dbName variable in the recipe or the one given during setup