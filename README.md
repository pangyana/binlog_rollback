# binlog_rollback
This python script is used to generating reverse SQL accoding to the binlog file. 
How to use?
shell> python binlog_rollback.py 
==========================================================================================
Command line options :
    --help                  # OUT : print help info
    -f, --binlog            # IN  : binlog file. (required)
    -o, --outfile           # OUT : output rollback sql file. (default 'rollback.sql')
    -h, --host              # IN  : host. (default '127.0.0.1')
    -u, --user              # IN  : user. (required)
    -p, --password          # IN  : password. (required)
    -P, --port              # IN  : port. (default 3306)
    --start-datetime        # IN  : start datetime. (default '1970-01-01 00:00:00')
    --stop-datetime         # IN  : stop datetime. default '2070-01-01 00:00:00'
    --start-position        # IN  : start position. (default '4')
    --stop-position         # IN  : stop position. (default '18446744073709551615')
    -d, --database          # IN  : List entries for just this database (No default value).
    --only-primary          # IN  : Only list primary key in where condition (default 0)

Sample :
   shell> python binlog_rollback.py -f 'mysql-bin.000001' -o '/tmp/rollback.sql' -h 192.168.0.1 -u 'user' -p 'pwd' -P 3307 -d dbname
==========================================================================================
