# Desafio_IA_Alura_Google

Aplicativo baseado na AI do Google (GEMINI).
Exibe sugestão de receitas, baseadas em um tempo máximo de preparo, quantidade de receitas e ingredientes.


Explicação do código:
Instalação do SDK: O código começa instalando o SDK do Google Generative AI usando o comando !pip install -q -U google-generativeai.
Configuração inicial:
Importa as bibliotecas necessárias, incluindo userdata para acessar dados do usuário no Google Colab e google.generativeai para interagir com o SDK.
Obtém a chave da API do Google Generative AI a partir dos dados do usuário usando userdata.get('API_KEY_1').
Configura o SDK com a chave da API usando genai.configure(api_key=api_key).
Configurações de geração e segurança:
Define as configurações de geração de texto, controlando o número de candidatos e a criatividade.
Define as configurações de segurança para bloquear conteúdo inadequado, neste caso, optando por não bloquear nenhum tipo de conteúdo.
Carregamento do modelo:
Carrega o modelo de linguagem "gemini-1.5-pro-latest" usando genai.GenerativeModel(), passando as configurações de geração e segurança definidas.
Loop de solicitação de receitas:
Inicia um loop while que continua até que o usuário insira 0 para a quantidade de receitas.
Dentro do loop, solicita ao usuário a quantidade de receitas, o tempo máximo de preparo e os ingredientes desejados.
Monta a solicitação para o modelo de linguagem, incluindo as informações fornecidas pelo usuário.
Usa o modelo de linguagem para gerar sugestões de receitas com base na solicitação, chamando model.generate_content(Solicitacao).
Imprime as sugestões de receitas geradas pelo modelo.
Finalização:
Sai do loop quando o usuário digita 0 para a quantidade de receitas.
Imprime a mensagem "## Fim ##" para indicar o término do programa.
