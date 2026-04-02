# Demo-DrawIO

Using Image from https://github.com/jgraph/docker-drawio

## origin
docker run \
    -it \
    -m1g \
    -v "./drawiodata/letsencrypt-log:/var/log/letsencrypt/" \
    -v "./drawiodata/letsencrypt-etc:/etc/letsencrypt/" \
    -v "./drawiodata/letsencrypt-lib:/var/lib/letsencrypt" \
    -e LETS_ENCRYPT_ENABLED=true \
    -e PUBLIC_DNS=localhost \
    --rm \
    --name="draw" \ 
    -p 87:80 \
    -p 447:8443 \ 
    jgraph/drawio

## Mit kubectl
```bash
kubectl create -f drawio.yaml
```

URL Result: https://localhost:447/