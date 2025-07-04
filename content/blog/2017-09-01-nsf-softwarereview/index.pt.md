---
slug: nf-softwarereview
title: Como a rOpenSci usa a revisão de código para promover a ciência reprodutível
crossposts:
- name: NumFOCUS blog
  url: https://numfocus.org/blog/how-ropensci-uses-code-review-to-promote-reproducible-science
preface: NumFOCUS is a nonprofit that supports and promotes world-class, innovative,
  open source scientific computing, including rOpenSci.
date: '2017-09-01'
author:
- Noam Ross
- Scott Chamberlain
- Karthik Ram
- Maëlle Salmon
topicid: 850
translator: Francesca Belem Lopes Palmeira
tags:
- software
- Software Peer Review
- community
params:
  doi: 10.59350/4y3kj-1re56
---

Na rOpenSci, criamos e organizamos softwares para ajudar os(as) cientistas no ciclo de vida dos dados. Essas ferramentas acessam, baixam, gerenciam e arquivam dados científicos de forma aberta e reprodutível. Logo no início, percebemos que isso só poderia ser um esforço da comunidade. A variedade de dados científicos e fluxos de trabalho só poderia ser resolvida com a contribuição de cientistas com conhecimentos específicos da área.

Com a abordagem da comunidade, surgiram desafios. **Como poderíamos garantir a qualidade do código escrito por cientistas sem treinamento formal em práticas de desenvolvimento de software? Como poderíamos promover a adoção de práticas recomendadas entre nossos(as) colaboradores(as)? Como poderíamos criar uma comunidade com pessoas que apoiariam umas as outras nesse trabalho?**

**Tivemos muito sucesso ao lidar com esses desafios por meio da *revisão por pares*.** Extraímos elementos de um processo familiar à nossa comunidade-alvo - a *avaliação acadêmica por pares* - e uma prática do mundo do desenvolvimento de software - a *revisão do código de produção* - para criar um sistema que promova a qualidade do software, a educação contínua e o desenvolvimento da comunidade.

## Um processo de revisão aberto

**Revisão de software de produção** ocorre em equipes de desenvolvimento de software, de código aberto ou não. As contribuições para um projeto de software são revisadas por um ou mais membros da equipe antes de serem incorporadas ao código-fonte do projeto. Normalmente, as contribuições são pequenos patches, e a revisão serve como uma verificação da qualidade, bem como uma oportunidade de treinamento nos padrões da equipe.

**Na revisão acadêmica por pares** as pessoas avaliadoras externas criticam um produto completo, geralmente um manuscrito, com um mandato muito amplo para abordar quaisquer áreas que considerem deficientes. A revisão acadêmica geralmente é anônima e, ao passar por ela, o produto e o(a) autor(a) recebem uma marca pública de validação.

**Nós combinamos essas abordagens.** Em nosso processo, as pessoas autoras enviam pacotes completos do R para a rOpenSci. Os(As) editores(as) verificam se os pacotes se enquadram no escopo do nosso projeto, executam uma série de testes automatizados para garantir uma linha de base de qualidade e integridade do código e, em seguida, designam duas pessoas revisoras independentes. Os(As) revisores(as) fazem comentários sobre a usabilidade, a qualidade e o estilo do código do software, bem como sobre a documentação. Os(As) autores(as) fazem alterações em resposta e, quando os(as) revisores(as) estiverem satisfeitos com as atualizações, o pacote recebe um selo de aprovação e passa a fazer parte do nosso pacote.

Esse processo é bastante iterativo. Depois que os(as) revisores(as) publicam uma primeira rodada de revisões extensas, os(as) autores(as) e revisores(as) conversam em um bate-papo informal, moderado apenas levemente por um(a) editor(a). Isso permite que tanto as pessoas revisoras quanto as autoras façam perguntas umas as outras e expliquem as diferenças de opinião. Isso pode ocorrer em um ritmo muito mais rápido do que a correspondência típica de revisão acadêmica. Usamos o sistema de problemas do GitHub para essa conversa, e as respostas levam de minutos a dias, em vez de semanas a meses.

**A troca também é aberta e pública**. Pessoas autoras, revisoras e editoras conhecem as identidades umas das outras. A comunidade mais ampla pode ver ou até mesmo participar da conversa enquanto ela acontece. Isso incentiva você a ser minucioso e a fazer revisões construtivas e não contraditórias. Tanto as pessoas autoras quanto as revisoras relatam que gostam e aprendem mais com essa troca aberta e direta. Isso também traz o benefício de criar uma comunidade. As pessoas participantes têm a oportunidade de se relacionar de forma significativa com novos(as) colegas, e novas colaborações surgiram por meio de ideias geradas durante o processo de revisão.

Estamos cientes de que os sistemas abertos podem ter desvantagens. Por exemplo, na revisão acadêmica tradicional, a revisão por pares duplamente cega [pode aumentar a representação de autoras do sexo feminino](https://www.sciencedirect.com/science/article/pii/S0169534707002704) sugerindo preconceito em revisões não cegas. Também é possível que as pessoas revisoras sejam menos críticas na revisão aberta. No entanto, afirmamos que a abertura da conversa sobre a revisão fornece uma verificação da qualidade e da parcialidade da revisão; é mais difícil injetar comentários subjetivos ou sem embasamento em público e sem a cobertura do anonimato. Em última análise, acreditamos que a capacidade das pessoas autoras e revisoras de se comunicarem direta e publicamente melhora a qualidade e a imparcialidade.

## Orientação e padrões

**A rOpenSci fornece orientação sobre a revisão.** Isso se divide em duas categorias principais: **práticas recomendadas de alto nível** e **padrões de baixo nível**. As práticas recomendadas de alto nível são gerais e amplamente aplicáveis a todas as linguagens e aplicativos. São práticas como "Escreva funções reutilizáveis em vez de repetir o mesmo código", "Teste casos extremos" ou "Escreva documentação para todas as suas funções". Devido à sua natureza geral, elas podem ser extraídas de outras fontes e não desenvolvidas do zero. Nossas práticas recomendadas são baseadas em orientações originalmente desenvolvidas pelo [Laboratório de Ciências da Mozilla](https://mozillascience.github.io/codeReview/intro.html).

Os padrões de baixo nível são específicos para uma linguagem (no nosso caso, R), aplicativos (interfaces de dados) e base de usuários(as) (pesquisadores). Eles incluem itens específicos, como convenções de nomenclatura para funções, melhores escolhas de dependências para determinadas tarefas e adesão a um guia de estilo de código. Temos um conjunto extenso de padrões para nossos(as) revisores(as) verificarem. Eles mudam com o tempo, à medida que o ecossistema do software R evolui, as práticas recomendadas mudam e as ferramentas e os recursos educacionais disponibilizam novos métodos para as pessoas desenvolvedoras.

**Nossos padrões também mudam com base no feedback dos(as) revisores(as).** Adotamos em nossos padrões sugestões que surgem de várias pessoas revisoras em diferentes pacotes. Descobrimos que muitas delas têm a ver com a facilidade de uso e a consistência das APIs de software e com o tipo e o local das informações na documentação que facilitam a localização. Isso destaca uma das vantagens de pessoas revisoras externas: elas podem oferecer uma nova perspectiva sobre a usabilidade, além de testar o software em casos de uso diferentes dos imaginados pelo(a) autor(a).

**À medida que os nossos padrões se tornaram mais abrangentes, passamos a confiar mais em ferramentas automatizadas.** O ecossistema do R, como a maioria das linguagens, tem um conjunto de ferramentas para code linting, teste de função, análise de código estático e integração contínua. Exigimos que os(as) autores(as) as utilizem, e os(as) editores(as) executam os envios por meio de um conjunto de testes antes de enviá-los para revisão. Isso libera as pessoas revisoras do fardo das tarefas de menor nível para que se concentrem nas críticas de maior nível, onde podem agregar mais valor.

## A comunidade de revisores

Um dos principais desafios e recompensas de nosso trabalho tem sido o desenvolvimento de uma comunidade de revisores.

**A revisão é uma atividade de alta habilidade.** As pessoas revisoras precisam ter conhecimento dos métodos de programação usados em um pacote de software e também do campo científico de sua aplicação ("Encontre-me alguém que conheça ecologia sensorial e estruturas de dados esparsas!"). Elas precisam de boas habilidades de comunicação e de tempo e disposição para se voluntariar. Felizmente, os mundos da ciência aberta e do código aberto estão repletos de pessoas generosas e especializadas. Conseguimos expandir o nosso grupo de revisores à medida que o ritmo dos envios e os domínios de suas aplicações aumentaram.

O desenvolvimento do grupo de revisores exige recrutamento constante. Nossos(as) editores(as) se envolvem de forma ativa e ampla com as comunidades de desenvolvedores e pesquisadores para encontrar novas pessoas revisoras. Recrutamos autores de envios anteriores, colegas de trabalho e colegas, em conferências, por meio de outros trabalhos colaborativos e nas mídias sociais. No ecossistema de software de código aberto, muitas vezes é possível identificar pessoas com conhecimentos específicos observando seus softwares publicados ou sua contribuição para outros projetos, e muitas vezes enviamos e-mails sem contato prévio para possíveis revisores cujo os trabalhos publicados sugerem que essas pessoas seriam uma boa opção para um envio.

Cultivamos nosso grupo de revisores e também o expandimos. Trazemos pessoas revisoras de volta para que elas possam desenvolver a revisão como habilidade, mas não com tanta frequência a ponto de sobrecarregá-las. Fornecemos orientação e feedback a recrutas iniciantes. Ao designar revisores para uma submissão, o nosso objetivo é juntar pessoas revisoras experientes com as iniciantes, ou as com experiência nos métodos de programação de um pacote com aquelas experientes em seu campo de aplicação. **Essas pessoas revisoras aprendem umas com as outras, e a diversidade de perspectivas é uma vantagem.** As pessoas desenvolvedoras menos experientes geralmente fornecem insights que as mais experientes não têm sobre a usabilidade do software, o design da API e a documentação. As pessoas desenvolvedoras mais experientes identificarão com mais frequência ineficiências no código, armadilhas devido a casos extremos ou sugerirão abordagens de implementação alternativas.

## Expansão da revisão por pares para código

A revisão de código tem sido uma das melhores iniciativas da rOpenSci. Criamos software, desenvolvemos habilidades e criamos comunidade, e o processo de revisão por pares tem sido um importante catalisador para todos os três. Ele tornou o software que desenvolvemos internamente e o que aceitamos de pessoas colaboradoras externas mais confiável, utilizável e passível de manutenção. Assim **estamos trabalhando para promover a revisão aberta de código por pares por mais organizações** que trabalham com software científico. Ajudamos a lançar o [The Journal of Open Source Software](https://joss.theoj.org/) que usa uma versão do nosso processo de revisão para oferecer um local de publicação favorável à pessoa desenvolvedora. O sucesso do JOSS levou a um spin-off, o [The Journal of Open Source Education](https://jose.theoj.org/) que usa um processo aberto, semelhante à revisão de código, para fornecer feedback sobre currículos e materiais educacionais. Também estamos desenvolvendo um programa piloto em que os artigos de software enviados a uma revista acadêmica parceira recebem um selo por passarem pela revisão da rOpenSci. Somos incentivados por outras iniciativas de revisão, como [ReScience](https://rescience.github.io/) e [O historiador da programação](https://programminghistorian.org/). As revisões de código da [BioConductor](https://www.bioconductor.org/), que antecedem as nossas por vários anos, recentemente mudaram para um modelo aberto.

**Se a sua organização estiver desenvolvendo ou fazendo a curadoria de códigos científicos, acreditamos que a revisão de código, bem implementada, pode ser um grande benefício. Você pode precisar de um esforço considerável para começar, mas **aqui estão algumas das principais lições que aprendemos e que podem ajudar você:**

- **Desenvolver padrões e diretrizes** para que autores e revisores da sua organização usem. Pegue-os emprestados livremente de outros projetos (sinta-se à vontade para usar os nossos) e modifique-os iterativamente à medida que você avança.
- **Use ferramentas automatizadas** como code linters, conjuntos de testes e medidas de cobertura de testes para reduzir ao máximo a carga das pessoas autoras, revisoras e editoras.
- **Tenha um escopo claro.** Explique a vocês mesmos e as possíveis pessoas colaboradoras o que o projeto aceitará e por quê. Isso evitará muita confusão e esforço no futuro.
- **Crie uma comunidade** por meio de incentivos de networking, oportunidades de aprendizado e gentileza.

**A rOpenSci está ansiosa para trabalhar com outros grupos interessados em desenvolver processos de revisão semelhantes**, especialmente se você tiver interesse em revisar e curar software científico em linguagens diferentes do R ou além do nosso escopo de suporte ao ciclo de vida dos dados. O software que implementa algoritmos estatísticos, por exemplo, é uma área propícia para a revisão aberta de código por pares. Por favor, [entre em contato conosco](/contact/) se você tiver dúvidas ou quiser co-pilotar um sistema de revisão para o seu projeto.

E, é claro, se você quiser fazer revisões, estamos sempre procurando voluntários(as). Inscreva-se em /onboarding.

***

Você pode apoiar a rOpenSci [tornando-se uma pessoa membro do NumFOCUS](https://www.numfocus.org/community/donate/) ou fazendo uma [doação para o projeto](https://www.numfocus.org/open-source-projects/).


