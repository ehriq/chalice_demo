# Tutorial de chalice

## O que vamos construir?

Uma aplicação para acompanhar a leitura e dar notas a livros. 

Essa aplicação é composta de:

+ Um endpoint para criar um nome de usuário para uma pessoa
+ Um endpoint para a pessoa registrar o andamento da leitura do livro
+ Um endpoint para a pessoa registrar uma avaliação para o livro
+ Um endpoint para a pessoa ver todos os livros que já leu
+ Uma tarefa agendada que diariamente notifica as pessoa sobre os livros que ainda está lendo.

Com isso, vamos ver um exemplo de como o chalice trabalha com:

+ API Gateway
+ SQS
+ Cloudwatch Events

## Pre requisitos 

+ Python 3.7 (usando virtualenv)
+ Variáveis de ambiente configuradas para interagir com o AWS
+ Comando `aws` configurado corretamente

# Instalando o chalice

Com o virtualenv ativo, rodar:

	(venv) $ pip install boto3 chalice awscli

E, ao terminar, verificar se o chalice está funcionando:

	(venv) $ chalice 

E o retorno será algo como:

	chalice 1.14.0, python 3.7.7, linux 5.4.0-7626-generic

Com isso, podemos **criar** nosso projeto com o comando:

	$ chalice new-project books

Esse comando cria o diretório `books/`, onde vai ficar o nosso projeto. Ao entrar nesse diretório, existem alguns itens:

+ `app.py` é o ponto de entrada da aplicação.
+ `.chalice` é o diretório onde ficam as configurações da aplicação. 
+ `requirements.txt` é o arquivo de controle de bibliotecas para o python.