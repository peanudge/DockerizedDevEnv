# "Dev Container" Project Template

This project is template for docker based development environment.

VSCode extension (Dev Container): ms-vscode-remote.remote-containers

1. Start "dev-env" docker image

"docker-compose.yaml" setups .NET dev environment image and SQL Server 2022 image

Run docker images

```bash
cd ./docker
docker compose up
```

Check "dev-env" instance

```bash
docker exec -it dev-env /bin/bash
dotnet --version
dotnet-ef --version
```

Check "sql_server" instance

```bash
docker exec -it sql_server /bin/bash
/opt/mssql-tools/bin/sqlcmd -S localhost -U SA
Password: Password1
1> SELECT @@VERSION
2> GO
```

2. In VScode, Open command menu, and search for "Remote-Container: Rebuild and Reopen in Container"

