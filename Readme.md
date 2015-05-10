## *Goal*
Raw-sql-migrate is replacement for South migration system without ORM using raw sql.

## *Usage*
This package provides python api. In order to use it just import api module.
```python
from raw_sql_migrate import api
```

### *Creating new migration*
In order to create new migration just call create method:
```python
api.create(package, name='', config='')
```
Calling of it will create new history migrations history table,
migrations directory in the package and py migration file
Example:
```python
api.create('package_a.package_b', name='initial')
```

### *Migration forward*
In order to migrate forward call
```python
api.forward(package, head=False, config='')
```