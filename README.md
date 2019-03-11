# consul-vault-install
\ ** bash script to install consul vault **\

1. change consul replica and bootstrap based on worker nodes

2. change namespace on script

3 . Vault Access

kubectl port-forward  pod/vault-6db48b8965-cxrc2 8200:8200

export VAULT_ADDR=https://127.0.0.1:8200

export VAULT_SKIP_VERIFY=1

vault status

4. expose node port for vault login inside cluster

eg : 
kubectl expose pod vault-54769fc9c-58ncz -n consul --port=8200 --target-port=8200 --external-ip=10.240.0.4 --type=NodePort

 
