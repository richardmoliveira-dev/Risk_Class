# Risk_Class

# Modelo de Classificação de Risco, conforme o protocolo de Manchester.
Este modelo foi primeiramente implentado em Maschaster, Inglaterra, e depois espalhou-se pelo mundo.
Consiste basicamente em ouvir as queixas dos pacientes, aferir seus sinais vitais (temperatura, saturação do oxigênio, batimentos cardíacos etc. e estabelecer o grau de urgência do atendimento, priorizando, obviamente, os casos mais graves. 

# Classificação de risco
São cinco classificações: que vai do vermelho ao azul, sendo o vermelho o mais grave.
Cores e respectivos tempos de atendimento: "vermelho - atendimento imediato"; laranja - atendimento em até 10 minutos; "amarelo - atendimento em até 60 minutos";
"verde - atendimento em até 120 minutos"; e "azul - atendimento em até 240 minutos.

# Uso do Gemini para geração dos textos simulando a conversa entre atendente e paciente
Eu Utilizei o Gemini para gerar os textos simulando a conversa entre a atendente do setor de triagem do hospital e o paciente, segundo o protoloco de Manchester.
Gerei uns 10 casos, distribuídos entre os vários de níveis de classificação. Fiz uma análise dos resultados e pedi para o Gemini refinar a resposta e responder de 
forma mais objetiva, sobretudo quanto a classificação de risco. 

# GOOGLE AI STUDIO
Então iniciei uma conversa no Google AI Studio. Eu colei inicialmente 5 textos que haviam sido gerados no Gemini com respectivas respostas de classficações de risco, para treinar o modelo. Em seguida, comecei a colar os outros textos e pedir para ele classicar. O modelo estava com dificuldade de separar os casos vermelhos do laranja. Os casos que ele errou eu corrigi com a resposta certa. Quando ele começou a acertar com mais frequência eu utilizei o recurso de clicar no botão "Gerar Código".

# Geração do Código em Python do modelo
Gerei o código e colei no Gooble Colab. O Código estava praticamente 100% pronto. No local de colar a API Key eu utilizei a dica do Fabrício para não expor a API Key. O modelo recebe um texto com a simulação de diálogo entre a atendente e o paciente e retorna a classificação de risco, que vai orientar a atendente a colocação da pulseira no paciente.

# Nota: 
A ideia original era utilizar áudios, simulando que a conversa entre atendentes e pacientes fosse captada pelo modelo, assim como as informações vitais dos pacientes, como forma de agilizar o atendimento. Como resultado o modelo iria retornar a classificação de risco por meio de voz.
