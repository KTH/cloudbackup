# cloudbackup
Tools to make local backups of hosted services.

## Requirements

### PostgreSQL client
PATH must contain a sufficiently new pg_dump. See https://www.postgresql.org/download/

### Borg
BorgBackup must be installed. Distribution packages are recommended. See: https://borgbackup.readthedocs.io/en/stable/installation.html

### Users
Create one user for each cloud or local cluster of databases.

### Disk space
A directory with sufficient disk space must be available. Recommended is to create directories and mount filesystems under /srv.

## Preparations
A borg repo must be initialized:

```bash
export BORG_REPO=/srv/cloudbackup/azure/mycloud
borg init -e none
```

# Running

For example:

```bash
 cloudbackup backup azure all
```

# Monitoring

Monitor the exit code from the command and log its output.
