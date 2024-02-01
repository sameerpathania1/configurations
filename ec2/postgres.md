postgres configuration ec2

1. sudo apt install postgresql
2. edit file /etc/postgresql/*/main/postgresql.conf
	uncomment code and set to 
	listen_addresses = '*'
3. sudo -u postgres psql template1
	ALTER USER postgres with encrypted password 'password123';
5. edit file /etc/postgresql/*/main/pg_hba.conf
	host all       all        0.0.0.0/0        scram-sha-256
6. sudo systemctl restart postgresql.service