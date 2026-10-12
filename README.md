# minecraft-server-container

Container baseline for a Paper instance with persistent world data, explicit UID, health probe, and conservative JVM memory sizing. It is a reference deployment, not a replacement for backups or host-level isolation.

## Run
Set a pinned image digest and persist `/data`; accept the EULA only after reviewing Mojang's terms. Never publish RCON or backend ports directly to the internet.

```sh
docker compose up -d
```

Tune memory below the container limit to leave room for native memory and the OS. Benchmark startup, saves, and peak player load on target hardware. MIT licensed.
