# Dba, our db tools, powered by ruby

## Features

* manage db config in one place 
* use favored command tools eg. pgcli, psql, sequel
* connect as easy as possible 
* write sqlets(db script) quickly
* make test and run easily
* try and learn advanced db knowledge

## Quick start

* config `~/.dbs.yml`(or `DBSFILE` env) as `sample-dbs.yml`
* install ruby locally eg. `brew install ruby` 
* install pg locally eg. `brew install postgresql@9.6`
* run `bundle install`
* put `source /path/to/here/dba.rc` in your `~/.bashrc`

### Try

run like below:

```
dbcli help
dbmigrate help
pga help
rake demo
sql/demo.rb
rspec spec/try_db_spec.rb 
```

## Used in starup

### pull staging db to local

* `pga gen_datafile postgres://xxx/to_staging_db` 
  生成大表过滤规则文件(如`.datafiles/starup.pg.staging.localdomain.5432.yml`)
* `pga copy postgres://src_staging_db_url/db1 postgres://localhost/new_not_exist_db1 --dryrun` 
  会生成导出shell语句，去掉--dryrun可立即copy，会定制生产的shell语句

## Inspired by

* https://github.com/Microsoft/pgtester
* https://medium.com/yammer-engineering/testing-postgresql-scripts-with-rspec-and-pg-tester-c3c6c1679aec
