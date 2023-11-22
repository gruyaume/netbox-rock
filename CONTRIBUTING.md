# Contributing

## Build and deploy

```bash
rockcraft pack -v
rock_version=$(yq '.version' rockcraft.yaml)
sudo skopeo --insecure-policy copy oci-archive:netbox_${rock_version}_amd64.rock docker-daemon:netbox:${rock_version}
docker run netbox:${rock_version}
```
