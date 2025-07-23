Домашнее задание курса OTUS "PostgreSQL для Альфа-Банк"

**Яшин Евгений Юрьевич**

**Используется:**

Welcome to Ubuntu 24.04.2 LTS (GNU/Linux 6.8.0-1030-raspi aarch64)

postgresql/noble-updates,now 16+257build1.1 a

**настойки:**


# Add settings for extensions here

max_connections = 50

shared_buffers = 2GB

effective_cache_size = 5GB

maintenance_work_mem = 512MB

checkpoint_completion_target = 0.9

wal_buffers = 16MB

default_statistics_target = 100

random_page_cost = 1.2

effective_io_concurrency = 200

work_mem = 4MB

min_wal_size = 1GB

max_wal_size = 2GB

max_worker_processes = 4

max_parallel_workers_per_gather = 2

max_parallel_workers = 4

max_parallel_maintenance_workers = 2



**скорость:**

sudo -u postgres  pgbench -c 8 -P 6 -T 60 -U postgres postgres
tps = 662.012128 (without initial connection time)
