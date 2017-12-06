to use your own data:

create symbolic links in the cruize directory:
```bash
ln -s /path/to/gbdb /path/to/cruize/gbdb
ln -s /path/to/mysqldata /path/to/cruize/sql
```


to run blat from a different computer without using docker:
```bash

# download gfServer if you don't already have (url to gfServer below assumes x86_64 architecture)
mkdir -p ~/cruize/bin/
curl -so ~/cruize/bin/gfServer http://hgdownload.cse.ucsc.edu/admin/exe/linux.x86_64/blat/gfServer
chmod +x ~/cruize/bin/gfServer
export PATH=${HOME}/cruize/bin:$PATH

# define your google spreadsheet ID
export DBDBID=1ilMW4gv8XsECFuKpSlOFWVhO_04qiogVdQHYYxQF2ZM

# define browser URL/IP
export FQDN=genomaize.us

bash <(curl -s https://raw.githubusercontent.com/FSUgenomics/cruize_scripts/master/start_blat_dockerless)

```

