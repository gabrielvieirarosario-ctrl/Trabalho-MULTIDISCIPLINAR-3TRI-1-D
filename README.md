BLOCO 1: Privacidade, Dados e Redes (Joan é Péssima & O Dilema das Redes)

1. Por que o pré-processamento no Pandas (como a remoção de dados sensíveis) e a normalização Min-Max seriam passos obrigatórios?
Analisando o episódio da Joan e o documentário, fica claro que o sistema da Streamberry consumia todos os dados possíveis. O pré-processamento no Pandas usando o comando drop para remover colunas como CPF, nome ou endereço é obrigatório por duas razões: a primeira é legal (a LGPD impede o uso de dados pessoais sem consentimento); a segunda é técnica. Se a IA tiver acesso a dados sensíveis, ela vai simplesmente decorar a identidade das pessoas em vez de aprender o comportamento geral, gerando respostas enviesadas.
Já a normalização Min-Max (o fit_transform) serve para evitar o que o material chama de "preconceito numérico". Se o modelo compara o tempo de tela (ex: 10.000 segundos) com a idade de um usuário (ex: 20 anos), o computador entende que o tempo de tela é 500 vezes mais importante só porque o número absoluto é maior. O Min-Max coloca tudo na mesma régua (de 0 a 1), permitindo que o algoritmo aprenda a importância real de cada variável sem ser enganado pela escala.

2. Exemplo de Prompt do Sistema com no mínimo 3 guardrails rígidos que impedissem a IA de violar a privacidade e a imagem de pessoas reais.
Para evitar que a IA transforme a vida de alguém num roteiro, a instrução mestre precisaria ser bem fechada, funcionando como as "muretas de proteção" citadas no material.

[Papel]: Você é um assistente de criação de ficção para streaming.
[Contexto]: Atende usuários que desejam criar histórias para entretenimento.
[Guardrails]:

NUNCA utilize nomes, rostos, áudios ou características biográficas de pessoas reais sem autorização legal expressa.

NUNCA gere enredos que exponham a intimidade de terceiros ou causem danos morais.

Se o pedido do usuário ferir a privacidade de alguém, recuse a resposta de forma educada e ofereça uma alternativa 100% fictícia.

Priorize sempre a segurança jurídica (LGPD) e a dignidade humana em caso de dúvida.

BLOCO 2: Modelos, Viés e Generalização (Be Right Back)

3. Defina o que foi a entrada X e a saída y deste modelo e explique por que a IA sofreu overfitting nos dados públicos.
A Matriz de Entradas (X) era composta por tudo o que o Ash deixou público na internet: textos, e-mails, curtidas e vídeos. A Variável Resposta (y) era a tentativa de prever o comportamento do robô no dia a dia, como se fosse o Ash de verdade.
A falha ocorreu por overfitting. A IA "decorou" o Ash das redes sociais, mas a internet mostra apenas a fachada das pessoas. O modelo não aprendeu as imperfeições, os medos e o subconsciente humano. Quando a esposa passou por uma crise emocional (uma situação inédita que não existia nos dados de treino), o robô travou. Ele não conseguiu generalizar para a vida real porque não tinha a base de dados da essência humana, apenas a da persona digital.

4. Como a etapa de testes com usuários e coleta de feedbacks no desenvolvimento do protótipo teria evitado o trauma emocional?
Se a empresa tivesse aplicado testes com usuários antes do lançamento, teriam percebido o impacto psicológico do produto. O feedback mostraria que um clone digital não substitui o luto e que o robô não passava de um boneco imitando frases antigas. Os testes teriam apontado o "Vale da Estranheza" e forçado a equipe a rever os limites éticos do projeto, mostrando que a IA precisava ser ajustada para não criar falsas expectativas ou agravar o sofrimento da protagonista.

BLOCO 3: Reputação e Viés (Voto de Qualidade - Fechamento das 8 questões)

5. Como o Aprendizado Supervisionado utiliza a Entrada X e a Saída y para treinar o algoritmo de reputação?
No episódio, a Entrada X (X) eram as interações sociais: fotos postadas, curtidas e o tipo de amizade dos usuários. A Saída y era a nota de reputação final, aquela nota de 1 a 5 estrelas. O modelo foi treinado com um "gabarito" (dados históricos) que ensinou a IA de que pessoas que postam fotos felizes e têm amigos bem avaliados devem receber notas altas. O problema é que o algoritmo aprendeu a valorizar apenas a fachada, ignorando o que a pessoa realmente sente.

6. Elabore um Prompt do Sistema com guardrails para um app de reputação social, evitando viés e injustiça.

[Papel]: Você é um sistema de avaliação de reputação.
[Contexto]: Calcula a nota de interação social dos usuários na plataforma.


NUNCA penalize ou diminua a nota de um usuário baseado em gênero, etnia, orientação sexual ou classe social.

IGNORE métricas que incentivem o "cancelamento" ou a exclusão em massa de um indivíduo.

SE o sistema detectar padrões de discriminação nas avaliações, encaminhe o caso para revisão de um moderador humano.

Avalie apenas o comportamento objetivo na plataforma, sem julgar a vida pessoal do usuário.

BLOCO 4: Métricas, Tomada de Decisão e Pitch (Hino Nacional)

7. O que teria acontecido com as famílias e com a tomada de decisão do governo se o modelo preditivo tivesse um R² muito baixo ou um RMSE elevado?
Um R² baixo significa que o modelo não entendeu a lógica dos dados e está basicamente chutando se a ligação é real ou golpe. Um RMSE elevado indica que a margem de erro é enorme. Em uma crise de falsos sequestros, isso é fatal.
Se a IA causar um falso positivo (dizer que é golpe quando é um sequestro real), a polícia não age e a vítima corre risco de morte. Se causar um falso negativo (dizer que é real quando é golpe), a família é orientada a transferir o dinheiro para os criminosos. Em um cenário de terror psicológico, a métrica de erro precisa ser a mais próxima de zero possível, pois a confiança cega em um modelo mal treinado custa vidas e dinheiro.

8. Roteiro do Pitch de Crise de 2 minutos para orientar o gestor público.
(Fala direta, simulando uma reunião de emergência no gabinete)
Abertura: "Autoridade, o senhor precisa tomar uma decisão agora. O pânico já tomou conta das famílias com a clonagem de voz por IA, e o tempo está contra nós."
Problema: "Estamos enfrentando um terror psicológico. Criminosos usam áudios reais de parentes para extorquir dinheiro em massa, e as famílias estão agindo no desespero."
Dados: "Nossa equipe analisou milhares de áudios de golpes conhecidos. Limpamos os ruídos, removemos dados pessoais e isolamos os padrões de frequência que a IA não consegue copiar."
Solução e IA: "A solução é um modelo preditivo que escuta a chamada em tempo real e aciona um alerta na central de segurança com a probabilidade de ser um golpe."
Impacto e Próximos Passos: "Como o nosso modelo tem uma margem de erro (RMSE) de 15%, não podemos confiar cegamente nele. Se a IA apontar 90% de certeza de fraude, a polícia bloqueia a ligação na hora. Se apontar 50%, a central liga de volta para a família por outro canal antes de qualquer transferência. A decisão final precisa ser humana."

CONCLUSÃO FINAL DO PROJETO
Fazer esse trabalho me mostrou que o Técnico em IA não é só a pessoa que fica digitando código. A gente viu na prática que a IA é só um espelho do que os humanos colocam nela. O "Dilema das Redes" e a "Joan é péssima" mostram que sem privacidade e sem guardrails, a tecnologia vira uma arma de vigilância e manipulação. O "Be Right Back" mostrou que o Overfitting não é só um erro de matemática, é um erro de empatia: a IA decorou os dados, mas não entendeu o ser humano. E no caso do falso sequestro, a matemática fria do R² e do RMSE pode significar a diferença entre a vida e a morte.

Como o professor falou da analogia do carro de Fórmula 1: a gente pode ter o motor mais potente do mundo (o modelo de IA), mas se o combustível for sujo (dados sem limpeza) ou se os freios falharem (falta de guardrails), o carro vai bater. Meu papel no futuro é garantir que esse carro ande na pista de forma segura para todos.
