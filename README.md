# Vector Role

Устанавливает и настраивает Vector.

## Что делает

- Создаёт каталоги установки и конфигурации
- Скачивает и распаковывает архив Vector
- Создаёт symlink на бинарник
- Копирует конфиг `vector.toml`
- Устанавливает systemd‑unit и запускает сервис

## Переменные

### Defaults

- `vector_version`: версия Vector (по умолчанию `0.37.0`)
- `vector_install_dir`: каталог установки (по умолчанию `/opt/vector`)
- `vector_config_dir`: каталог конфига (по умолчанию `/etc/vector`)
- `vector_archive`: имя архива (по умолчанию `vector-{{ vector_version }}-x86_64-unknown-linux-gnu.tar.gz`)
- `vector_download_url`: URL архива
- `vector_extract_dir`: каталог распаковки
- `vector_symlink_path`: путь к бинарнику (по умолчанию `/usr/bin/vector`)

## Пример использования

```yaml
- name: Install Vector
  hosts: vector
  become: true
  roles:
    - vector-role
```
