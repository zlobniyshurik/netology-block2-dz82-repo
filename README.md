# netology-block2-dz82-repo

## Краткое описание:

Ansible Playbook для установки на **RHEL**оподобные дистрибутивы ПО **`Clickhouse`** и **`Vector`**.

----

## Список устанавливаемых компонентов при настройках по умолчанию:

**[Clickhouse](https://clickhouse.com/) версии `22.3.3.44`:**  
- clickhouse-client
- clickhouse-server
- clickhouse-common-static

----
**[Vector](https://vector.dev) версии `0.21.2`:**
- vector

----

## Настройки:

### Inventory:

Файл **[playbook/inventory/prod.yml](./playbook/inventory/prod.yml)** со списком хостов, на которых запускается playbook.

### Переменные с настройками:

Расположены в файле **[playbook/group_vars/clickhouse/vars.yml](./playbook/group_vars/clickhouse/vars.yml)**:  

**`clickhouse_packages`** - список устанавливаемых пакетов для `Clickhouse`

**`clickhouse_version`** - версия пакетов с `Clickhouse`  
*Сейчас там `22.3.3.44`*  

**`vector_arch`** - архитектура пакетов *(armv7/aarch64/x86_64)*  
*Правда, до тех пор, пока `Clickhouse` имеет готовые rpm только для архитектуры `x86_64`, `armv7/aarch64` смысла выбирать не имеет.*  

**`vector_packages`** - список устанавливаемых пакетов для `Vector`  

**`vector_rpm_build`** - версия RPM билда пакетов для `Vector`
*Сейчас там `1`*  

**`vector_version`** - версия пакетов с `Vector`  
*Сейчас там `0.21.2`*

----
