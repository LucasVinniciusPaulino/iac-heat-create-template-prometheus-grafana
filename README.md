# Projeto de Infraestrutura com Grafana e Prometheus utilizando IAC Heat

# Descrição
Este projeto utiliza a IAC Heat da OpenStack para provisionar uma infraestrutura completa que inclui Grafana, Prometheus e Node Exporter, este template automatiza a criação de redes, sub-redes, roteadores, grupos de segurança, volumes e servidores, configurando também Prometheus para coletar métricas e Grafana para visualização.

# Objetivo
O objetivo deste projeto é fornecer uma infraestrutura escalável e monitorada, pronta para uso em ambientes de desenvolvimento e produção na OpenStack. Ele simplifica a criação e o gerenciamento de recursos de monitoramento essenciais para operações contínuas e eficientes.

# Funcionalidades
- Automatização de Infraestrutura: Utilização do Heat para definir redes, sub-redes, roteadores e grupos de segurança.
- Monitoramento com Prometheus: Configuração do Prometheus para coletar métricas de servidores e aplicações.
- Visualização com Grafana: Implementação do Grafana para criar dashboards personalizados e visualizar métricas em tempo real.
- Escalabilidade: Capacidade de adicionar mais servidores e ajustar recursos conforme necessário.

# Recursos Utilizados
## Neutron
- Network: dmz_network
- Subnet: dmz_subnet
- Router: router
- Router Interface: dmz_router_interface
- Security Group: dmz_security_group
- Floating IP: server1_floating_ip, server2_floating_ip, server3_floating_ip
- Floating IP Association: server1_floating_ip_association, server2_floating_ip_association, server3_floating_ip_association
## Cinder
- Volume de boot: my_vol1, my_vol2, my_vol3
## Nova
- Instance: server1, server2, server3
## Recursos server1
- Prometheus: Configuração do Prometheus para coletar métricas de todos os servidores.
- Grafana:
          Docker Container (Contêiner Docker): Configuração do Grafana em um contêiner Docker para visualização de métricas.
          Dashboard (Painel de Controle): Utilização de um dashboard específico importado via JSON para visualização de métricas do Prometheus.
## Recursos server2
- Node Exporter: Implantação do Node Exporter para coletar métricas de hardware e sistema operacional.
## Recursos server3
- Node Exporter: Implantação do Node Exporter para coletar métricas de hardware e sistema operacional.
