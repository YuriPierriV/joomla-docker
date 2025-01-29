# Docker Joomla

Este repositório fornece uma configuração simples para executar uma instância do Joomla usando o Docker e Docker Compose. Com apenas um único comando, você pode ter um ambiente Joomla rodando localmente para desenvolvimento ou testes.

## Pré-requisitos

Certifique-se de ter o seguinte instalado em sua máquina:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Como usar

1. Clone este repositório:

   ```bash
   git clone https://github.com/YuriPierriV/joomla-docker.git
   cd joomla-docker
   ```

2. Suba os containers com o Docker Compose:

   ```bash
   docker-compose up
   ```

3. Acesse o Joomla no seu navegador:

   - Frontend: [http://localhost:8080](http://localhost:8080)
   - Backend (Admin): [http://localhost:8080/administrator](http://localhost:8080/administrator)

4. Configure o Joomla através da interface web.

## Estrutura do Repositório

```
.
├── db_data
├── joomla_data
├── .gitignore
└── docker-compose.yml
```

- **db_data**: Pasta de armazenamento do Mysql.
- **joomla_data**: Pasta de armazenamento dos arquivos Joomla.
- **docker-compose.yml**: Arquivo de configuração do Docker Compose.


## Configuração do `docker-compose.yml`

O `docker-compose.yml` já está configurado para subir dois serviços principais:

1. **Joomla**: Aplicação Joomla baseada na imagem oficial do Docker.
2. **MySQL**: Banco de dados necessário para o Joomla.

Se precisar de ajustes na configuração (como mudar portas ou credenciais), edite o arquivo `docker-compose.yml`.


## Observações

- Para acessar o Backend (Admin), [http://localhost:8080/administrator](http://localhost:8080/administrator), utilize:
    - USERNAME: `joomla` 
    - PASSWORD: `joomla@secured`
- Certifique-se de que a porta `8080` está livre no seu sistema.

## Limpeza

Para parar e remover os containers, use o seguinte comando:

```bash
docker-compose down
```

Se quiser remover também os volumes (dados do banco de dados), execute:

```bash
docker-compose down -v
```

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests.
