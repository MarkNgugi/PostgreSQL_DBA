## DDL Queries for managing schemas

### 1. Creating a schema/database

#### To create a new schema, you can use the CREATE SCHEMA command:
```
CREATE SCHEMA schema_name;
```
#### For example, to create a schema named sales:
```
CREATE SCHEMA sales;
```
### 2. Displaying available schemas

#### To view all available schemas within the current database:
```
SELECT * FROM information_schema.schemata;
```
### 3. Dropping a schema

### To drop a schema, use the DROP SCHEMA command. Be cautious when using this command as it will also delete all objects within the schema.

#### To drop a schema without deleting objects if any are present:
```
DROP SCHEMA IF EXISTS schema_name;
```
#### To delete a schema along with its contained objects:
```
DROP SCHEMA schema_name CASCADE;
```
### 4. Setting the search path

### When referring to a database object without specifying the schema, PostgreSQL will use the search path to resolve the object’s schema. By default, the search path is set to the public schema.

#### To change the search path, you can use the SET command:
```
SET search_path TO schema_name;
```
