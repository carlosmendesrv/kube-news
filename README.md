[![](https://kubedev.io/wp-content/uploads/2020/08/Artboard-1@2x.png)](https://kubedev.io/wp-content/uploads/2020/08/Artboard-1@2x.png)

## Desafio KubeDev
E pra encerrar o desafio, hora de colocar a aplicação Kube-News pra rodar no cluster. Então sua missão agora é criar o Dockerfile e os manifestos pra fazer o deploy. (coloca aqui o seu repositório no GitHub)


## Requisitos 

- Docker
- K3D
- Kubectl

## Executando o projeto

Executando o projeto
```bash
https://github.com/carlosmendesrv/kube-news
```

Criando Cluster com 3 agentes e 3 servers
```
k3d cluster create cluster-temperatura --agents 3 --servers 3 -p "8080:30000@loadbalancer"
```

Para realizar o Deploy da aplicação, vamos execlutar o arquivo deployment

```
kubectl apply -f src/k8s/deployment.yaml
```

O projeto estará disponível na seguinte url http://127.0.0.1:30000
