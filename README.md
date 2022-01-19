#Passos para criar o container da aplicação e subilo no cluster k8s

1- clonar o repositorio para a sua maquina local (git clone)

2- entrar localmente na pasta rotten-potatoes\src

3- Criar a imagem > Executar o comando "docker image build -t jpzanini/rotten-potatoes:tag"

4- Subir o container para o seu repositorio > Executar o comando "docker push jpzanini/rotten-potatoes:tag"

5- Criar o seu cluster > Executar o comando "k3d cluster create mycluster --agents 3 --servers 3 -p "8080:30000@loadbalancer" "

6- Aplicar o arquivo de deployment > Executar o comando "kubectl apply -f deployment.yaml"
