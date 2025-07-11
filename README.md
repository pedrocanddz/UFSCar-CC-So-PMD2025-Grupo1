# Resumo

&emsp;Analisar como a fintech Current adota tecnologias NoSQL, especificamente MongoDB e Neo4j, para atender às suas demandas de escalabilidade, flexibilidade e gestão de relacionamentos entre usuários. Esta análise busca contemplar a arquitetura adotada, os benefícios operacionais e os desafios enfrentados na integração com a Google Cloud, visando compreender como essas tecnologias impactam positivamente os serviços financeiros oferecidos. 

# Introdução
&emsp;O avanço das fintechs tem transformado significativamente o setor financeiro global. Fintech é a junção dos termos financial (financeiro) e technology (tecnologia), e define empresas que oferecem produtos e serviços financeiros por meio de plataformas digitais, eliminando a necessidade de agências físicas e processos burocráticos tradicionais. 

&emsp;Enquanto bancos convencionais operam com estruturas centralizadas, sistemas legados e processos muitas vezes engessados, as fintechs surgem com propostas baseadas em arquiteturas tecnológicas flexíveis, que permitem escalabilidade, redução de custos operacionais e melhor experiência para o usuário. Isso se torna ainda mais crítico em um cenário de alta competitividade, onde a capacidade de adaptar rapidamente produtos e serviços às necessidades dos clientes é desejado.

&emsp;É dentro desse contexto que a Current, uma fintech norte-americana, se consolida como um exemplo de inovação tecnológica aplicada aos serviços financeiros. A empresa oferece serviços como cartão de débito, antecipação de salário, controle de gastos e outras funcionalidades focadas na inclusão financeira e na simplicidade do uso. Seu público-alvo são principalmente trabalhadores assalariados que buscam uma alternativa mais ágil, barata e eficiente aos bancos tradicionais.

&emsp;Para viabilizar essa proposta, a Current precisou superar desafios comuns no setor bancário digital, como o processamento de um grande volume de transações em tempo real, a manutenção da consistência dos dados, a escalabilidade do sistema e a personalização dos serviços. As soluções tradicionais baseadas em bancos de dados relacionais não atendiam mais essas demandas de forma eficiente, principalmente em termos de performance, elasticidade e custo de operação. Por isso, a Current adotou uma arquitetura fundamentada em tecnologias NoSQL, utilizando dois pilares principais: o MongoDB e o Neo4j. 

&emsp;O MongoDB, banco de dados orientado a documentos, é utilizado para armazenar cada transação como um documento independente. Esse modelo permite que a fintech reconstrua o estado das contas dos usuários a qualquer momento com base no histórico de transações, adotando uma abordagem orientada a eventos, que garante alta performance, resiliência e escalabilidade horizontal. Por outro lado, o Neo4j, banco de dados orientado a grafos, foi implementado para modelar e gerenciar as conexões entre usuários como relações familiares, redes sociais e vínculos financeiros. Esse modelo é fundamental para oferecer funcionalidades personalizadas, como limites compartilhados, autorizações específicas e análises antifraude baseadas nas relações entre clientes. Consultas que seriam extremamente complexas e lentas em bancos relacionais são realizadas de forma muito mais eficiente e escalável utilizando grafos.

&emsp;Além disso, todo esse ecossistema está integrado à infraestrutura da Google Cloud, o que oferece elasticidade, segurança, alta disponibilidade e automação de processos operacionais. Entretanto, essa integração também traz desafios importantes, como a necessidade de garantir segurança, governança de dados, consistência em ambientes distribuídos e controle de custos operacionais na nuvem.

&emsp;Diante desse cenário, este trabalho tem como objetivo analisar como a fintech Current adota essas tecnologias para atender suas demandas operacionais, avaliar os benefícios e os desafios envolvidos nessa estratégia tecnológica, e compreender como essa arquitetura baseada em NoSQL contribui diretamente para a escalabilidade, flexibilidade e personalização dos serviços financeiros oferecidos.

# Objetivos 
&emsp;Este estudo tem como objetivo principal analisar como a fintech Current adota tecnologias NoSQL para atender suas demandas operacionais, de escalabilidade e personalização de serviços. Especificamente, busca-se compreender de que maneira o MongoDB é utilizado para armazenar cada transação como um documento individual, permitindo a reconstrução do estado das contas em tempo real por meio de um modelo orientado a eventos. Além disso, pretende-se entender como o banco de dados Neo4j é empregado na modelagem de relacionamentos sociais e familiares entre os usuários, possibilitando consultas mais eficientes, rápidas e personalizadas, que impactam diretamente a oferta de serviços financeiros diferenciados.

&emsp;Para alcançar esses objetivos, este trabalho se apoia em uma pesquisa qualitativa, fundamentada na análise do artigo oficial publicado pela MongoDB, que apresenta o estudo de caso da fintech Current e descreve a sua arquitetura tecnológica. A partir desse material, será possível interpretar, de maneira acessível, como a Current estrutura seu sistema para processar e armazenar transações utilizando MongoDB, bem como compreender como o modelo de reconstrução do estado das contas é implementado de forma eficiente em tempo real.

&emsp;A compreensão do uso do Neo4j será desenvolvida por meio da análise das informações disponibilizadas no artigo, complementada com levantamento documental sobre os princípios dos bancos de dados orientados a grafos. Isso permitirá entender de que forma a Current representa e consulta relações entre usuários, otimizando a entrega de serviços financeiros personalizados.

&emsp;Adicionalmente, o trabalho busca avaliar os benefícios e os desafios envolvidos na adoção dessas tecnologias, especialmente no contexto da integração com a Google Cloud, considerando aspectos como escalabilidade, consistência dos dados, segurança, governança e operação em ambientes de nuvem.

&emsp;Por fim, este relatório se propõe a investigar como a combinação dessas soluções como MongoDB, Neo4j e Google Cloud contribuíram para a flexibilidade da arquitetura da Current, para a escalabilidade horizontal do sistema e ampla disponibilidade do serviço. Ainda que baseado em fontes secundárias, este estudo busca oferecer uma análise interpretativa, aplicada e alinhada às práticas e desafios atuais do setor financeiro digital.

# Planejamento Inicial (Fase Intermediária I)
&emsp;O tema escolhido para a realização deste trabalho é a aplicação de tecnologias NoSQL na arquitetura da fintech Current, com foco na análise do uso dos bancos de dados MongoDB e Neo4j. O escopo do projeto está direcionado especificamente para compreender como essas tecnologias são utilizadas pela Current para garantir escalabilidade, flexibilidade e eficiência na gestão de dados transacionais e relacionais.

&emsp;A metodologia adotada consiste em uma pesquisa qualitativa baseada na análise do artigo oficial disponibilizado pela MongoDB, complementada por levantamento documental e estudo técnico sobre conceitos fundamentais relacionados aos bancos NoSQL, em especial aqueles orientados a documentos e a grafos.

&emsp;Para a organização e desenvolvimento do trabalho, as atividades foram divididas entre os integrantes do grupo, contemplando as seguintes etapas: realização de pesquisa teórica sobre o funcionamento e as aplicações do MongoDB e do Neo4j (Paulo); análise da arquitetura da Current, conforme descrito no artigo e em materiais complementares (Pedro); elaboração da produção textual, incluindo as seções de resumo, introdução (Pedro),  objetivos e fundamentação teórica (Paulo).

&emsp;O cronograma foi estruturado levando em consideração as entregas previstas nas fases I do projeto, garantindo que cada etapa fosse concluída dentro dos prazos estabelecidos, de forma a assegurar a qualidade do desenvolvimento e a coerência na apresentação dos resultados.

# Referências
https://www.mongodb.com/blog/post/next-generation-mobile-bank-current-using-mongodb-atlas-google-cloud-make-financial-services-accessible-affordable-all
