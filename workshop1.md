# Associate Google Cloud Engineer - Workshop 1

Good links
  - https://googlecloudcheatsheet.withgoogle.com/

Active Cloud Shell -> VM Gerenciada pela Google fora da sua rede, e com sdk instalado.
```gcloud compute instances list```

IAP para conectar na VM que nao tenha um IP externo.

Zonal Persistent Disk
Regional Persistent Disk
Local SSD -> cannot be persistent. Highest performance, lowest latency
Cloud Storage Bucket - > NAS

### Availability Policies


# Associate Google Cloud Engineer - Workshop 2
### Snapshot vs Image
Snapshot:
  - Fotografia atual. Aquele momento em especifico. Fazer um backup daquele momento especifico. Pode se ter muitas copias dessa imagem, e fazer scheduling de backups. Pode se deletar snapshot, marcando-os. Um snapshot so pode ser filho de uma image e so pai de outro snapshot

Images:
  - O inicio de tudo. A partir desta imagem, varias coisas podem acontecer. Tem-se um OS especifico, e quer-se levantar servidores a partir dela, a imagem sera melhor.

Snapshot te da um historico. O clone nao, mas ambos acabam sendo a mesma coisa. O snapshot seria um source control tool. Se nao ha essa necessidade, pode ser o clone. O snapshot 'e gravado no cloud storage.

Imagem publica: imagens prontas, como windows, debian, macos.
'E possivel criar uma propria images, mas que o OS atenda aos requisitos de architetura da google.
Snapshot takes longer to be uploaded than the image cause it needs to be restored. Imaghes are used to create bootdisks and templates
---
Criar sistema escalavel no GCP:
  criar instancia e2.
  trocar boot disk para debian 11, e keep bootdisk after deleting vm.
  allow http e load balancer.
  conectar via ssh
    sudo apt update
    sudo apt instal npm
    pwd
    mkdir www
    cd www
    npm init
    nano package.json
      
    npm install express
    www exit  
  Cotas/quotas.limits
  we can request is to be increasedm like the number of cpu`s
  ---
  An instance needs an IP to run properly on GCP

  VPC -> global scope resource
  VM -> conjunao de recursos em um IP. nao e uma maquina fisica
