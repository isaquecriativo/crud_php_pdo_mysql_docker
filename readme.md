# CRUD  com PHP, PDO, Mysql, Phpmyadmin no Docker

para rodar a aplicação precisar ter o docker e o docker-compose instalados 


https://www.docker.com/products/docker-desktop


Primeiro Crie um Diretorio na pasta raiz com o nome: database
para rodar a aplicação precisar ter o docker e o docker-compose instalados 

## Para rodar a aplicação execulte o comando

```
docker-compose up -d
```

## Criar banco de dados

Abra o pypmyadm no navegador com o endereço

http://127.0.0.1:8081/

### Crie um banco de dados com o nome web-vagas

Depois crie a tabela "vagas" por SQL

```
CREATE TABLE `vagas` (
  	`id` INT(11) NOT NULL AUTO_INCREMENT,
  	`titulo` VARCHAR(255) NOT NULL COLLATE 'utf8_general_ci',
  	`descricao` TEXT(65535) NOT NULL COLLATE 'utf8_general_ci',
  	`ativo` ENUM('s','n') NOT NULL COLLATE 'utf8_general_ci',
  	`data` TIMESTAMP NOT NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  	PRIMARY KEY (`id`) USING BTREE
  )
  COLLATE='utf8_general_ci'
  ENGINE=InnoDB
  AUTO_INCREMENT=1;
```
## Pronto agora é só testar! a aplicação no endereço

http://127.0.0.1:8080/index.php
