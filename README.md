# Install PostgreSQL 12 on Ubuntu

### Update System

    sudo apt update
    sudo apt -y install vim bash-completion wget
    sudo apt -y upgrade

A reboot is necessary after an upgrade.

    sudo reboot
    
 ### Add PostgreSQL 12 repository
 
    curl -fsSL https://www.postgresql.org/media/keys/ACCC4CF8.asc|sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/postgresql.gpg
    
    echo "deb http://apt.postgresql.org/pub/repos/apt/ `lsb_release -cs`-pgdg main" |sudo tee  /etc/apt/sources.list.d/pgdg.list
    
 ### Install PostgreSQL 12 on Ubuntu
 
    sudo apt update
    sudo apt -y install postgresql-12 postgresql-client-12
    
 Cek Status

    systemctl status postgresql.service
    
    systemctl status postgresql@12-main.service
    
### Test PostgreSQL Connection

access to your entire PostgreSQL instance

    sudo su - postgres
    
Let’s reset this user password to a strong Password we can remember.

    psql -c "alter user postgres with password 'ddi'"

Start PostgreSQL prompt by using the command:

    psql
    



    
