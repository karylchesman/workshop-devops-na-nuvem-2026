# AWS

## IAM

IAM User - qualquer usuários
IAM Role - perfis que permissões compartilhadas
IAM Trusted entity - específica quais entidades dentro da AWS podem usar a role através do `assume role`

Utilização de roles criam credenciais rotativas (temporárias)

## Networking

### VPC

**Virtual Private Cloud**, rede virtual privada dentro da cloud para isolar recursos.
Ao criar uma **VPC**, vai ser necessário definir o **CIDR** - Classless Inter Domain Routing, e isso vai definir a quantidade ips disponíveis na rede.

### AZ

**Availability Zone**, são conjuntos de datacenters distribuídos em locais geograficamente separados dentro de uma região da AWS. Isso ajuda a garantir disponibilidade e tolerância a falhas no caso de, por exemplo, problemas em datacenters de uma determinada região.

LoadBalancer precisam de no mínimo 2 **AZs**.

### Subnets

Existem as **Públicas e Privadas**.

Mas o que vai definir se ela é pública ou privada é as definições abaixo:

As **Públicas**, são subnets que estão associadas a uma tabela de roteamento, onde na sua rota padrão tem um apontamento para um **Internet Gateway**.
As **Privadas**, são associadas a uma tabela de roteamento, mas em vez do **Internet Gateway**, na sua rota padrão, terei o **NAT Gateway** opcionalmente.
