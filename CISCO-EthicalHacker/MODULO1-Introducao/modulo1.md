# Anotações

# Atores de Ameaças

### Crime organizado
grupos muito bem financiados e motivados que normalmente usarão todas e quaisquer técnicas de ataque mais recentes. Seja ransomware ou roubo de dados, se puder ser monetizado, o crime organizado o usará.

### Hacktivistas
Hacktivistas estão procurando fazer um ponto ou promover suas crenças, usando o crime cibernético como seu método de ataque

### Atacantes patrocinados pelo Estado
Guerra Cibernetica e Espionagem. Muitos governos ao redor do mundo hoje usam ataques cibernéticos para roubar informações de seus oponentes e causar perturbações. 

### Ameaças Internas
Ameaças internas geralmente são funcionários normais que são enganados para divulgar informações confidenciais ou clicar por engano em links que permitem que invasores tenham acesso aos seus computadores

# Metodologias de Teste de Penetração
Ao utilizar uma metodologia conhecida, você é capaz de fornecer documentação de um procedimento especializado que foi usado por muitas pessoas.

## Testes de infraestrutura de rede
Focado em avaliar a postura de segurança da infraestrutura de rede real e como ela é capaz de ajudar a se defender contra ataques.
- switches
- roteadores
- firewalls
- recursos de suporte, como servidores de autenticação, autorização e contabilidade (AAA) e IPSs.

## Testes baseados em aplicação
Este tipo de teste de penetração foca em testar fraquezas de segurança em aplicativos corporativos.
- configurações incorretas
- problemas de validação de entrada
- problemas de injeção e falhas lógicas

Como um aplicativo da web é normalmente construído em um servidor da web com um banco de dados back-end, o escopo do teste normalmente inclui o banco de dados também. No entanto, ele foca em **obter acesso a esse banco de dados de suporte** por meio do comprometimento do aplicativo da web. Um ótimo recurso é o Open Web Application Security Project (**OWASP**).

## Teste de penetração na nuvem
Os provedores de serviços de nuvem ( Cloud service providers - **CSPs**), como Azure, Amazon Web Services (AWS) e Google Cloud Platform (GCP), não têm escolha a não ser levar suas responsabilidades de segurança e conformidade muito a sério. 

 responsabilidade pela segurança da nuvem depende do tipo de modelo de nuvem (SaaS, PaaS ou  IaaS). Por exemplo, com **IaaS**, o cliente (consumidor da nuvem) é responsável por dados, aplicativos, tempo de execução, middleware, máquinas virtuais (VMs), contêineres e sistemas operacionais em VMs. Independentemente do modelo usado, a segurança da nuvem é responsabilidade do cliente e do provedor de nuvem

 No geral, você quer garantir que o CSP tenha as mesmas camadas de segurança (lógica, física e administrativa) em vigor que você teria para os serviços que controla. Ao executar testes de penetração na nuvem, você deve entender o que pode fazer e o que não pode fazer. 
 A maioria dos CSPs tem diretrizes detalhadas sobre como executar avaliações de segurança e testes de penetração na nuvem. Independentemente disso, há muitas ameaças potenciais quando as organizações mudam para um modelo de nuvem. Por exemplo, embora seus dados estejam na nuvem, eles devem residir em um local físico em algum lugar. Seu provedor de nuvem deve concordar por escrito em fornecer o nível de segurança necessário para seus clientes.

[!] Os programas de recompensa por bugs (Bug bounty) permitem que pesquisadores de segurança e testadores de penetração obtenham reconhecimento (**e frequentemente compensação monetária**) por encontrar vulnerabilidades em sites, aplicativos ou quaisquer outros tipos de sistemas. Empresas como Microsoft, Apple e Cisco e até mesmo instituições governamentais como o Departamento de Defesa dos EUA (DoD) usam programas de recompensa por bugs para recompensar profissionais de segurança quando encontram vulnerabilidades em seus sistemas
[GitHub](https://github.com/The-Art-of-Hacking/h4cker/tree/master/bug-bounties) 

---
## Teste de ambiente desconhecido (Black-Box)
o testador normalmente recebe apenas uma quantidade muito limitada de informações. 
Por exemplo, o testador pode receber apenas os nomes de domínio e endereços IP que estão no escopo de um alvo específico. **A ideia desse tipo de limitação é fazer com que o testador comece com a perspectiva que um invasor externo pode ter**.

Outro aspecto do teste em ambiente desconhecido é que às vezes o pessoal de suporte de rede do alvo pode não receber informações sobre exatamente quando o teste está ocorrendo. Isso permite que um exercício de defesa também ocorra e **elimina o problema de um alvo se preparando para o teste e não dando uma visão do mundo real** de como a postura de segurança realmente parece.
Em um teste de ambiente desconhecido, o escopo pode ser apenas identificar um caminho para a organização e parar por aí.

## Teste de ambiente conhecido (White-Box)
o testador começa com uma quantidade significativa de informações sobre a organização e sua infraestrutura. O testador normalmente receberia coisas como diagramas de rede, endereços IP, configurações e um conjunto de credenciais de usuário. **A ideia desse tipo de teste é identificar o máximo possível de falhas de segurança**.

Com o teste de ambiente conhecido, o escopo é normalmente muito mais amplo que o Blacak-Box e inclui auditoria de configuração de rede interna e varredura de computadores desktop em busca de defeitos. Tempo e dinheiro são normalmente fatores decisivos na determinação de qual tipo de teste de penetração concluir

## Teste de ambiente parcialmente conhecido (Gray-Box)
uma abordagem **híbrida** entre testes de ambiente **desconhecido e conhecido**. Com testes de ambiente parcialmente conhecido, os testadores **podem receber credenciais, mas não documentação completa** da infraestrutura de rede. Isso permitiria que os testadores ainda fornecessem resultados de seus testes da perspectiva do ponto de vista de um invasor externo.

---
## PRÁTICA
Tipos de Testes de Penetração

A Protego foi contratada para fazer um teste de infraestrutura de rede como parte de um engajamento de teste de penetração mais amplo. O que você estará almejando neste teste? (Escolha todas as opções aplicáveis.)

- [X] Dispositivos IPS
- [X] Servidores AAA
- A Vitrine Digital
- [X] Switches
- Maquinas Virtuais (VM) que estão sendo executadas na nuvem
 
> Os testes de infraestrutura de rede focam na avaliação da postura de segurança da infraestrutura de rede, incluindo switches, roteadores, firewalls, a infraestrutura sem fio e recursos de suporte. Eles também podem incluir servidores AAA e dispositivos IPS.


[I] Um breve Resumo sobre o que são cada coisa

#### IPS devices (Intrusion Prevention Systems)
são sistemas de segurança de rede projetados para monitorar o tráfego de dados em tempo real e prevenir ameaças, como ataques cibernéticos. Eles analisam pacotes de rede e podem bloquear tráfegos suspeitos automaticamente, complementando firewalls e outros mecanismos de proteção.

#### AAA servers (Authentication, Authorization, Accounting)
Servidores AAA são usados em segurança de redes para realizar três funções principais:
- Autenticação: Verifica a identidade de usuários ou dispositivos
- Autorização: Define quais recursos ou ações ou usuário/dispisitivo tem permissão para acessar
- Contabilidade: Regristra as atividades realizadas, como logs de acesso e uso.
Ex de Servidores AAA incluem RADIUS e TACACS+

#### The digital storefront
Refere-se a uma "loja digital" ou plataforma de comércio eletrônico. Essa infraestrutura permite que empresas vendam produtos ou serviços online, incluindo sites, aplicativos e interfaces de usuário projetadas para interação com os clientes.

#### Switches
Switches são dispositivos de rede que conectam vários dispositivos em uma mesma rede local (LAN), permitindo a comunicação eficiente entre eles. Eles operam na camada 2 (ou às vezes na camada 3) do modelo OSI, encaminhando pacotes de dados com base nos endereços MAC.

#### Virtual machines (VM) que estão sendo executadas na nuvem
Máquinas virtuais na nuvem são instâncias de computadores virtuais hospedados em provedores de serviços de nuvem, como AWS, Azure ou Google Cloud. Elas permitem executar sistemas operacionais e aplicativos de forma isolada, aproveitando os recursos escaláveis e flexíveis da nuvem.
---

## Levantamento de diferentes Padrões e metodologias
Há uma série de metodologias de teste de penetração que já existem há algum tempo e continuam sendo atualizadas conforme novas ameaças surgem.

### MITRE ATT&CK Framework
O framework [MITRE ATT&CK](https://attack.mitre.org) é um recurso incrível para aprender sobre as táticas, técnicas e procedimentos (TTPs) de um adversário. 
Tanto profissionais de segurança ofensiva (testadores de penetração, red teamers, caçadores de bugs e assim por diante) quanto respondedores de incidentes e equipes de caça a ameaças usam o framework MITRE ATT&CK hoje. 
O framework MITRE ATT&CK é uma coleção de diferentes matrizes de táticas, técnicas e subtécnicas. Essas matrizes — incluindo a Enterprise ATT&CK Matrix, Network, Cloud, ICS e Mobile — listam as táticas e técnicas que os adversários usam ao se preparar para um ataque, incluindo coleta de informações (inteligência de código aberto [OSINT], identificação de fraquezas técnicas e de pessoas e muito mais), bem como diferentes técnicas de exploração e pós-exploração.

### OWASP Web Security Testing Guide (WSTG)
O [OWASP Web Security Testing Guide (WSTG)](https://owasp.org/www-project-web-security-testing-guide/) é um guia abrangente focado em testes de aplicativos da web. É uma compilação de muitos anos de trabalho de membros do OWASP. 
O OWASP WSTG abrange as fases de alto nível dos testes de segurança de aplicativos da web e se aprofunda nos métodos de teste usados.
>Por exemplo, ele chega a fornecer vetores de ataque para testar ataques de script entre sites (XSS), XML external entity (XXE), cross-site request forgery (CSRF) e ataques de injeção de SQL; bem como como prevenir e mitigar esses ataques

### NIST SP 800-115
A [Special Publication (SP) 800-115](https://csrc.nist.gov/pubs/sp/800/115/final) é um documento criado pelo National Institute of Standards and Technology (NIST) ou (Instituto Nacional de Padrões e Tecnologia) que faz parte do Departamento de Comércio dos EUA. O NIST SP 800-115 fornece às organizações diretrizes sobre o planejamento e a condução de testes de segurança da informação. 
Ele substituiu o documento padrão anterior, SP 800-42.

É considerado um padrão da indústria para orientação de testes de penetração e é mencionado em muitos outros padrões e documentos da indústria

### Open Source Security Testing Methodology Manual (OSSTMM)
O Open Source Security Testing Methodology Manual (OSSTMM), desenvolvido por Pete Herzog, já existe há muito tempo. Distribuído pelo [Institute for Security and Open Methodologies (ISECOM)](https://www.isecom.org), o OSSTMM é um documento que estabelece testes de segurança repetíveis e consistentes. Atualmente, ele está na versão 3, e a versão 4 está em status de rascunho. O OSSTMM tem as seguintes seções principais:

- Métricas de Segurança Operacional
- Análise de Confiança
- Fluxo de trabalho
- Teste de Segurança Humana
- Teste de Segurança Física
- Teste de Segurança sem fio
- Testes de Segurança em Telecomunicações
- Testes se Segurança de Redes de Dados
- Regulamentos de conformidade
- Relatórios com o Security Test Audit Report (STAR)

### Penetration Testing Execution Standard (PTES)
O [Penetration Testing Execution Standard (PTES)](http://www.pentest-standard.org) fornece informações sobre tipos de ataques e métodos, e fornece informações sobre as últimas ferramentas disponíveis para realizar os métodos de teste descritos. O PTES envolve sete fases distintas:

- Interações pré-engajamento
- Coleta de informações
- Threat modeling
- Análise de vulnerabilidade
- Exploração
- Pós-exploração
- Relatórios

https://www.youtube.com/watch?v=WHKIxX_dYy8

### Information Systems Security Assessment Framework (ISSAF)
É outra metodologia de teste de penetração semelhante às outras nesta lista com algumas fases adicionais. O ISSAF abrange as seguintes fases:

- Coleta de informações
- Mapeamento de rede
- Identificação de vulnerabilidades
- Penetração
- Obtendo acesso e escalonamento de privilégios
- Enumerando mais
- Comprometendo usuários/sites remotos
- Manter o acesso
- Cobrindo os rastros
