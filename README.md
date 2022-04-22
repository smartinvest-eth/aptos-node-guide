# aptos-node-guide
Run fullNode + generate a unique static node identity with one-line script (docker)
If there was a new release update you can use same one-line script to renew your node. Your private key will stay the same

curl -s https://raw.githubusercontent.com/hungcc/aptos-node-guide/main/aptos-docker > aptos-docker.sh && chmod +x aptos-docker.sh && ./aptos-docker.sh

View public identity details
cat $HOME/aptos/identity/peer-info.yaml

View private key
cat $HOME/aptos/identity/private-key.txt

View logs
cd $HOME/aptos

docker compose logs -f --tail 1000

Stop node
cd $HOME/aptos

docker compose stop

Start node
cd $HOME/aptos

docker compose start

Delete node
cd $HOME/aptos

docker compose down -v

rm -rf $HOME/aptos
