🚀 Visão Geral do Projeto
O AdivinhaVerse foi projetado para oferecer uma experiência de jogo fluida, leve e responsiva. O sistema desafia o usuário a descobrir um número gerado aleatoriamente, fornecendo dicas visuais instantâneas:

🟢 Verde: Quando o palpite indica que o número secreto é maior (ou em caso de vitória/acerto).

🔴 Vermelho: Quando o palpite indica que o número secreto é menor.

🛠️ Prompts e Histórico de Refatoração
Durante o ciclo de desenvolvimento, evolução e refinamento da arquitetura do aplicativo, os seguintes prompts e diretrizes técnicas foram utilizados para otimizar o código, corrigir dependências e ajustar a interface:

1. Configuração e Conexão com o Firebase
Prompt utilizado:
"Configure a conexão com o Firebase utilizando o arquivo firebaseConfig.js com persistência de sessão e Firestore integrados de forma universal para React Native, prevenindo erros de inicialização duplicada (duplicate-app)."

Ajustes realizados: Implementação da verificação de instâncias existentes (getApps().length === 0) e configuração robusta do Firestore e Auth com suporte ao AsyncStorage.

2. Estilização Nativa e Modo Escuro (Dark Mode)
Prompt utilizado:
"Refatore o layout do componente principal (index.tsx) para operar exclusivamente em modo escuro profundo, substituindo propriedades incompatíveis e garantindo alta performance nativa sem dependências de estilização externas."

Ajustes realizados: Aplicação de uma paleta de cores consistente baseada em tons de azul escuro e chumbo (#0B0F19 e #131C2E), garantindo legibilidade e contraste adequado para ambientes com pouca luz.

3. Mecânica do Jogo e Feedback Visual por Cores
Prompt utilizado:
"Ajuste a lógica de validação de palpites para comparar o número inserido com o número sorteado (Math.floor(Math.random() * 100) + 1), alterando dinamicamente a cor da dica visual para verde quando o número alvo for maior e vermelho quando for menor."

Ajustes realizados: Criação de estados reativos para a cor da dica (corDica), tratamento de entradas inválidas e validação em tempo real das tentativas do jogador.

4. Integração do Ranking Global em Tempo Real
Prompt utilizado:
"Implemente a listagem de ranking utilizando escuta em tempo real (onSnapshot) do Firestore, ordenando os jogadores pelo menor número de tentativas de forma otimizada para dispositivos móveis."

Ajustes realizados: Conexão da coleção de pontuações (ranking_jogo) utilizando consultas ordenadas (orderBy, limit) para exibir o top 10 de forma instantânea na interface.

📱 Tecnologias Utilizadas
React Native / Expo

TypeScript

Firebase Firestore (Banco de dados em tempo real)

AsyncStorage (Persistência local)
