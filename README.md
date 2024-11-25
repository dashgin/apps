
# Docker Shortcuts Utilities

When I need to run a Docker Compose configuration, I often find myself searching for compose files and place to run them.
I added this repository to store the compose files and a script to run them.

## Project Structure

```
app1/
    data/
    docker-compose.yml
app2/
    data/
    docker-compose.yml
run
```

## Usage

### Running the Script

To use the 

run

 script, follow these steps:

1. **Add the script to your PATH**:
   ```sh
   ln -s /path/to/run.sh /usr/local/bin/run-container
   ```
   This will allow you to use the `run-container` command from anywhere.

2. **Run the script**:
   ```sh
   run-docker <folder> [flag]
   ```

   - `<folder>`: The name of the folder containing the 

docker-compose.yml

 file you want to run.
   - `[flag]`: Optional flag to control the behavior of the script.

### Examples

- **Start services**:
  ```sh
  run-docker kafka
  ```

- **Start services in detached mode**:
  ```sh
  run-docker kafka -d
  ```

- **Stop services**:
  ```sh
  run-docker kafka -down
  ```

- **Stop services and remove volumes**:
  ```sh
  run-docker kafka -down-v
  ```

### Flags

- `-d`: Run services in detached mode.
- `-down`: Stop services.
- `-down-v`: Stop services and remove volumes.

## Supported Applications

The following applications are supported with their respective Docker Compose configurations:

- Minio
- MongoDB
- pgAdmin
- PostgreSQL

Each application has its own folder containing the 

docker-compose.yml

 file and any necessary data directories.

## License

This project is licensed under the MIT License. See the LICENSE file for details.