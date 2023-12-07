# Automatizando-a-Cria-o-de-Recursos-AWS-com-Terraform

# Automatizando a Criação de Recursos AWS com Terraform

Este projeto tem como objetivo fornecer uma solução automatizada para a criação de recursos na AWS utilizando Terraform. A automação é realizada por meio de um ambiente Dockerizado, executando em um sistema operacional Linux. O projeto inclui scripts Dockerfile, Terraform e AWS para facilitar a replicação e execução em diferentes ambientes.

## Pré-requisitos
- Docker instalado
- Acesso à AWS (chaves de acesso configuradas)

## Configuração do Ambiente Docker

O Dockerfile fornecido cria um ambiente contendo as ferramentas necessárias para a execução do Terraform e AWS CLI.

1. Utilize a imagem oficial do Ubuntu como base.
2. Atualize os pacotes do sistema e instale dependências necessárias.
3. Defina a versão do Terraform e baixe e instale-o.
4. Crie a pasta /lab1 dentro do container.
5. Copie main.tf para a pasta /lab1 no container.
6. Crie a pasta Downloads e instale o AWS CLI para acessar a AWS.

## Terraform Configuration (main.tf)

O arquivo `main.tf` contém as configurações específicas do Terraform para a criação de uma instância EC2 na região `us-east-2`.

1. Configure o provedor AWS na região us-east-2.
2. Defina os parâmetros da instância EC2, como AMI e tipo de instância.
3. Adicione tags à instância para identificação.

## Executando o Terraform

Certifique-se de configurar suas credenciais da AWS antes de executar o Terraform. Isso pode ser feito por meio do AWS CLI ou configurando as variáveis de ambiente `AWS_ACCESS_KEY_ID` e `AWS_SECRET_ACCESS_KEY`.

1. Execute `terraform init` para inicializar o projeto.
2. Execute `terraform apply` para criar os recursos na AWS.

## Considerações Finais

Este projeto é uma base para a automação de criação de recursos AWS com Terraform. Sinta-se à vontade para ajustar as configurações conforme necessário para atender às suas necessidades específicas. Para mais informações sobre o Terraform, consulte a [documentação oficial](https://www.terraform.io/docs/index.html).
