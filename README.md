# evan.network RPC node

The evan.network rpc node provides access to Blockchain via RPC API calls. These are HTTPS and WebSocket calls made from the DAPPs. The RPC server requires a fixed public IP and is inserted into the DNS LoadBalancing of the evan.network as a node. Connections to the server are stateless and encrypted. The certificate is provided by EVAN. network.

## Requirements

The technical requirements to the installed server are :
AWS:
 - T2.xlarge /T2.large Instance
 - Min. 300GB EBS storage

Azure:
 - Standard_D4_v3 / Standard_D2_v3
 - Min 300GB Premium storage

OnPremise:
 - 2 Xeon CPU's
 - 16GB RAM
 - 300GB SSD storage

DigitalOcean:
- Standard droplet with
- 8GB RAM, 4 vCPU, 160gb SSD

Open Ports:

30303 (TCP & UDP) – Blockchain Sync

80 - HTTP

443 - HTTPS

- 1 fixed IP public address

To start the RPC node you must have installed [docker](https://www.docker.com/get-docker) and [docker-compose](https://docs.docker.com/compose/install/) on your Server

## Configuration

Nothing to configure

## Starting

To start your rpc node, you have to simply run "docker-compose up -d" in the directory.

## Logging

To access the log file from the authoritynode, you can use the command "docker logs -f --tail 1000 RUNNING_CONTAINER_NAME" to get the last 1000 log lines from the container. The RUNNING_CONTAINER_NAME can be replaced with the following names:

- parity_rpc (The blockchain instance)
- nginx_parity (NGINX reverse proxy)

## Troubleshooting

If any of the nodes behave wrong, you can restart the container with the command "docker restart RUNNING_CONTAINER_NAME"

Please reach out our support team with the last logs of your container, to check if there's anything wrong.
