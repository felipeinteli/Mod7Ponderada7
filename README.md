# Módulo 7 Ponderada Semana 6

# Proposta de Aprendizado Contínuo para Chatbot de Fintech B2B

## Introdução

A atualização contínua de modelos em sistemas conversacionais é crucial para manter a relevância e eficácia desses sistemas. No contexto de uma fintech B2B que utiliza um chatbot para atendimento de vendedores, o desafio é manter o sistema atualizado com as mudanças constantes em produtos (alteração nos retornos do webhooks por exemplo), terminologias, regulamentações e necessidades dos usuários. O conceito de *concept drift* refere-se à mudança nos padrões subjacentes dos dados ao longo do tempo, o que pode diminuir a precisão dos modelos de aprendizado de máquina se não forem atualizados adequadamente.

## Solução Proposta

A solução proposta envolve a implementação um chatbot de sistema de dialógo com aprendizado contínuo inspirado no framework apresentado no artigo, que utiliza ontologias para melhorar a compreensão e a geração de respostas do chatbot. Este sistema será composto por vários blocos modulares, cada um com responsabilidades específicas:

1. **Conexão do Usuário:** Este módulo gerencia todas as interfaces dos canais de comunicação, como texto e áudio, e converte todas as mensagens recebidas para um formato específico (InputMessage), permitindo que o sistema processe todos os tipos de mensagens de forma uniforme.

2. **NLU (Compreensão de Linguagem Natural):** Interpreta as mensagens do usuário, extraindo informações semânticas úteis, como intenções e entidades, que auxiliam o sistema a responder de forma adequada, produzindo um Documento Semântico com todas as informações relevantes.

3. **Belief Tracker:** Atualiza o estado atual da caixa de diálogo com base na nova mensagem do usuário, mantendo uma memória de curto prazo das informações mencionadas anteriormente na conversa.

4. **Política:** Observa o estado atual do diálogo e seleciona a ação mais apropriada a ser tomada pelo agente, baseando-se em regras ou algoritmos de aprendizado de máquina.

5. **NLG (Geração de Linguagem Natural):** Transforma a ação escolhida pela política em uma frase em linguagem natural, que é enviada de volta ao usuário pelo mesmo canal de comunicação utilizado para a mensagem original.

6. **Gestão do Conhecimento:** Responsável por gerenciar o conhecimento do domínio, buscando informações em APIs externas, ontologias ou bancos de dados relacionais para fornecer dados aos módulos Belief Tracker e Policy.

7. **App Gate:** Atua como um conector entre o sistema de diálogo e aplicações externas. Após um diálogo suficiente para uma operação específica, aciona a ação para que este módulo solicite a operação à aplicação, cujo resultado é retornado ao sistema de diálogo para inclusão na resposta.

8. **Autenticação do Usuário:** Autentica o usuário quando uma operação é solicitada, diferenciando entre perguntas informativas e transacionais, onde a autenticação é necessária para realizar tarefas específicas.

Cada bloco terá a responsabilidade de garantir que o sistema se mantenha atualizado e relevante, adaptando-se continuamente às mudanças no ambiente e nas necessidades dos usuários.


### Uso de Ontologias

As ontologias desempenham um papel crucial na estruturação do conhecimento dentro do sistema. Elas permitem que o chatbot compreenda e processe as interações dos usuários de maneira mais eficaz, identificando conceitos e relações específicas do domínio da fintech. Por exemplo, uma ontologia pode definir conceitos como "consulta de saldo", "desaverbação de saldo do FGTS", "criação de usuários" e "dados sobre comissão", bem como as relações entre esses conceitos. Isso não apenas melhora a capacidade do chatbot de fornecer respostas precisas, mas também facilita a identificação de novas áreas de conhecimento que precisam ser incorporadas ao sistema.

## Conclusão

A implementação de um sistema de aprendizado contínuo em um chatbot de uma fintech B2B é uma tarefa de alta complexidade que demanda mão de obra qualifica e um tempo relevante para desenvolvimento, porém a longo prazo é uma grande vantagem competitiva para manter a eficácia do atendimento e a satisfação dos usuários, podendo justificar seu investimento dependendo seu custo de oportunidade. A abordagem modular e o foco no aprendizado contínuo oferecem uma estrutura flexível e escalável que pode se adaptar às mudanças do mercado e às necessidades dos usuários.

## Referências Bibliográficas

- Artigo base: "A Modular Framework for Domain-Specific Conversational Systems Powered by Never-Ending Learning". Applied Sciences. Disponível em: [https://www.mdpi.com/2076-3417/14/4/1585](https://www.mdpi.com/2076-3417/14/4/1585).
