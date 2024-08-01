Passos desenvolvidos:

1 - Criação de uma pipeline no CodePipeline
    - Foi criado 3 steps na pipeline: Source, Build, Deploy.
        - Na etapa Source, foi feita a conexão com o GitHub para obtenção do código fonte da aplicação e o arquivo de buildspec para a pipeline;
        - Na etapa do Build, foi onde ocorreu a etapa da construção da imagem do Docker com a aplicação, e o envio para o repositório privado no ECR. Aqui tive um pouco de dificuldade com alguns erros que foram solucionados com acerto de permissão e correção de comandos no buildspec;
        - Na etapa do Deploy, a imagem era enviada para produção no ElasticBeanstalk. Não tive sucesso nessa etapa, pois estava enfrentando algumas dificuldades com a configuração do ElasticBeanstalk.

2 - Criação de um repositório privado no ECR

3 - Criação de uma aplicação do ElasticBeanstalk
    - Aqui tive dificuldades e não consegui evoluir com a disponibilização do ambiente.

Considerações: Ao inves do ElasticBeanstalk, poderia ter utilizado o ECS ou EKS, o que poderia me ajudar a poupar tempo. Também poderia ter configurado a pipeline através do GitHub Actions, e só apontar para o destino na AWS. Outro ponto seria consolidar todas as configurações feitas em arquivos Terraform, garantindo assim a reusabilidade.
