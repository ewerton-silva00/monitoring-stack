# monitoring-stack
Stack de Monitoramento

**Passo 01**: Criar uma rede externa chamda ```public_network```.
```bash
docker network create public_network
```

**Passo 02:** Adicionar no ```/etc/hosts``` do seu notebook/computador o DNS de cada serviço apontando para ```localhost```
```bash
127.0.0.1 traefik.meudominio.local
127.0.0.1 prometheus.meudominio.local
127.0.0.1 alertmanager.meudominio.local
127.0.0.1 karma.meudominio.local
127.0.0.1 grafana.meudominio.local
127.0.0.1 portainer.meudominio.local
127.0.0.1 consul.meudominio.local
127.0.0.1 chat.meudominio.local
127.0.0.1 cadvisor.meudominio.local
```

**Passo 03:** Inicializar a stack.
```bash
docker-compose up --detach
```