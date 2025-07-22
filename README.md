# Database schema documentation for open msupply

This repository is used to show open msupply schema with schemaspy on github pages.

You would need to generate postgres schema first in [open-msupply repository](https://github.com/msupply-foundation/open-msupply) `cargo run --bin remote_server_cli --features postgres -- initialise-database`

Then using schemaspy docker create schema: `docker run -v "$PWD/docs/2.9.0:/output" -v "$PWD/schemaspy.properties:/schemaspy.properties" schemaspy/schemaspy:latest`

`NOTE`, version would need to be changed, and if generating on linux you may need to change `schemaspy.host` property, as it doesn't bind 'docker.host.internal' (can also do `--add-host host.docker.internal:host-gateway` as docker param).

After committing generate schema to main you should see it on: `https://msupply-foundation.github.io/open-msupply-database-schema/2.9.0`

