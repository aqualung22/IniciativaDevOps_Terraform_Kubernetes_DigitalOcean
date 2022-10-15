## Provisionamento de IaC com Terraform e implantação de cluster Kubernetes na Digital Ocean

O Terraform é uma ferramenta de Hashicorp que implementa o conceito IaC , Infra as a Code , e permite construir, alterar e versionar a infraestrutura de forma segura e eficiente.

No desafio, foi utilizada a cloud da Digital Ocean.

A IaC foi declarada utilizando a linguagem proprietária HCL - Hashicorp Configuration Language. Com ela, podemos declarar blocos dos tipos 
- Resource: criação de elemento gerenciado pelo Terraform
- Data Source: acesso a APIs e outros states Terraform
- Provider: plugins, chamados de providers, permitem conexão com cloud providers, API e outros
- Variable: definição de variáveis
- Output: exibição de dados na saída do console

Instalado o cloud Provider da Digital Ocean, para vincular o acesso da máquina local Linux à cloud.

Declarada e aplicada a configuração inicial da infraestrutura, com recurso Size padrão. Logo após, foi acrescentado um Nodepool Premium e verificado que sua aplicação seria efetivada "à quente".

Reutilização de código e parametrização: token de acesso, nome do cluster Kubernetes e da região do cloud provider extraídos para outro arquivo.

Instalado um local Provider para obter da Digital Ocean o arquivo de configuração do Kubectl, para manipular o cluster remoto.

Realizado o deployment de uma aplicação NodeJs e de um banco de dados PostgreSQL em um cluster Kubernetes e verificado o estado dos nodes, pods, service, deployment, load balancer e conferido o acesso externo à aplicação pelo navegador.


