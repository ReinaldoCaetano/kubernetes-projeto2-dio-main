<h1> Colocando uma aplicação em produção CI - CD (A cada commit no git-lab atualiza aplicação e coloca em produção automaticamente) usando docker, kubernetes, google cloud, mysql,php,git-lab</h1>

  <strong>Pré-requistos</strong>

🔸Docker e Docker compose
🔸kubectl
🔸gcloud (Conexão ao cluster da gcloud, criação de chaves e mv)


  <strong>Para executar basta cadastro git-lab e configurar </strong> 

```
git config --global user.name "NomeDeUsuario"
git config --global user.email "seuemail@gitlab.com"
```

  <strong> Basta ir para diretorio </strong>

```
git init --initial-branch=main
git remote add origin https://gitlab.com/seurepositorio/seurepositorio
git add .
git commit -m "Initial commit"
git push -u origin main

```



​   <strong> Durante o teste caso de algum erro de acesso na porta 3306 e 80 é preciso liberar firewall</strong>

```
gcloud compute firewall-rules create my-app-k8s --allow tcp:3306
gcloud compute firewall-rules create my-app-k8s --allow tcp:80

```