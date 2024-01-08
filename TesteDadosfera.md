# Item Troubleshooting

### Imagine que você é um analista de suporte e recebe um chamado do cliente reportando um problema na importação dos dados da Dadosfera. Você deve responder como se estivesse interagindo com o cliente no atendimento do chamado. O erro ocorreu nesta pipeline de coleta na Dadosfera. Sugira a alteração a ser feita no Dataset e escreva sobre outros cuidados que nosso usuário deve ter quando carregar dados do Google Sheets para a plataforma. Utilize a documentação da Dadosfera para entender como baixar os logs.

- Olá! Verificamos que a coleta de dados ocorreu com sucesso, talvez você tenha tido algum problema com relação ao formato da planilha no google sheets. Em futuras importações de dados, caso sua planilha tenha sido criada no Excel e carregada para o Google Drive, ela será salva com a extensão xlsx ou xls. Antes de realizar a coleta dela para a Dadosfera, certifique se o arquivo continua nesses formatos. Caso não tenha sido realizada a mudança de extensão automaticamente, vá em: Arquivo > Salvar como Planilhas Google.

![Sucesso ao realizar importação](https://github.com/Pedroaguilar1232/PEDRO_ALMEIDA_DDF_SUPORTE_2023_01/blob/main/images/sucesso.png)

# Item Processos Internos

### Imagine que a Dadosfera está passando por um upgrade e incorporando uma nova plataforma de gerenciamento de diretório em nuvem, com SSO e recursos de ciclo de vida do usuário. Como você organiza e implementa esses marcos para garantir uma transição suave e eficiente? Isso pode impactar o caso anterior? Explique como se daria cada interação com a base de clientes, de forma que eles se preparem para a mudança.

- É essencial comunicar aos usuários sobre a data dessa atualização para que eles se planejem para possíveis intabilidades na plataforma, essa atualização pode sim impactar nas pipelines de importação de dados. É importante treinar e capacitar  os funcionários, especialmente aqueles envolvidos no gerenciamento de dados e interação com clientes; disponibilizar recursos de autoatendimento, como manuais e tutoriais, para facilitar a adaptação dos usuários; disponibilizar canais de suporte eficientes para lidar com dúvidas ou problemas dos clientes durante e após a transição; manter uma equipe de suporte dedicada para ajudar os clientes durante o período de adaptação; implementar um sistema de monitoramento contínuo para identificar rapidamente quaisquer problemas após a transição e tomar medidas corretivas.

# Item Boas-Práticas de Suporte

### Suponha que você tenha acesso a uma ferramenta de Chatbot com AI robusta que possa ser integrada à Dadosfera para melhorar a interação do cliente. Como você implementaria essa ferramenta para melhorar a satisfação e o envolvimento do cliente? Desenhe o processo do fluxo do processo de atendimento, incluindo interações entre usuário, máquina (IA como o GPT ou outra), documentação (docs.dadosfera.ai) e humano (Suporte Dadosfera). Exemplifique, com um print de um prompt e uma resposta, como que uma IA poderia ajudar nesse atendimento. Sugerimos o uso de ChatGPT ou Bard.

- Identificação de Necessidades do Cliente:
Os clientes interagem com a plataforma buscando informações, suporte ou solução para seus problemas.

- Integração de IA Generativa (GPT ou Outra):
Implementação de um modelo de IA generativa (como o GPT) na plataforma para entender e responder automaticamente às consultas dos clientes.

- "Alimentação" da base de conhecimento do chatbot:
A IA é alimentada com conhecimentos sobre a plataforma, baseando suas respostas na documentação fornecida pela Dadosfera.

- Geração de Respostas Contextualmente Relevantes:
Com base nas interações e conhecimento adquirido, a IA gera respostas contextualmente relevantes e personalizadas, oferecendo informações úteis.

- Feedback do Usuário:
Após a resposta gerada pela IA, o sistema solicita feedback do usuário para avaliar a satisfação e corrigir possíveis imprecisões.

- Intervenção Humana (Suporte Dadosfera):
Se a IA não puder fornecer uma resposta satisfatória ou se o usuário solicitar, a interação é encaminhada para um agente do Suporte Dadosfera.

- Histórico e Documentação Automática:
Todas as interações (IA e humana) são registradas automaticamente para criar um histórico. O sistema também documenta respostas frequentes e soluções para ampliar sua base de conhecimento.

- Melhorias Contínuas com Aprendizado de Máquina:
O sistema é atualizado continuamente com base no feedback do usuário. A IA aprende com interações passadas para melhorar suas respostas e precisão.

- Monitoramento da Satisfação do Cliente:
Ferramentas analíticas monitoram a satisfação do cliente, avaliando feedbacks e métricas relacionadas para garantir melhorias contínuas.

- Atualizações de Documentação:
Com base nas interações, a documentação é atualizada regularmente para garantir que a IA e os agentes humanos tenham acesso às informações mais recentes.

![Exemplo de prompt e  resposta](https://github.com/Pedroaguilar1232/PEDRO_ALMEIDA_DDF_SUPORTE_2023_01/blob/main/images/chatbot.png).

# Item Consultas SQL

### Na Dadosfera, temos uma base de dados com informações fictícias de uma empresa. Foi demandado pela sua liderança de Customer Service que crie análises descritivas da própria área com base nesses dados. Você pode ver mais detalhes aqui neste link. Utilize as mesmas credenciais para acessar nosso módulo de Visualização.

```
SELECT "source"."GENDER" AS "GENDER", COUNT(*) AS "count"
FROM (SELECT "PUBLIC"."TB__TAEZZB__EMPLOYEE"."AGE" AS "AGE", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."BUSINESSTRAVEL" AS "BUSINESSTRAVEL", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."DEPARTMENT" AS "DEPARTMENT", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."DISTANCEFROMHOME" AS "DISTANCEFROMHOME", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."EDUCATION" AS "EDUCATION", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."EDUCATIONFIELD" AS "EDUCATIONFIELD", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."EMPLOYEECOUNT" AS "EMPLOYEECOUNT", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."EMPLOYEENUMBER" AS "EMPLOYEENUMBER", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."GENDER" AS "GENDER", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."JOBLEVEL" AS "JOBLEVEL", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."JOBROLE" AS "JOBROLE", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."MARITALSTATUS" AS "MARITALSTATUS", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."NUMCOMPANIESWORKED" AS "NUMCOMPANIESWORKED", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."OVER18" AS "OVER18", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."OVERTIME" AS "OVERTIME", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."TOTALWORKINGYEARS" AS "TOTALWORKINGYEARS", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."YEARSATCOMPANY" AS "YEARSATCOMPANY", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."YEARSINCURRENTROLE" AS "YEARSINCURRENTROLE", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."YEARSSINCELASTPROMOTION" AS "YEARSSINCELASTPROMOTION", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."YEARSWITHCURRMANAGER" AS "YEARSWITHCURRMANAGER", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."__SDC_ROW" AS "__SDC_ROW", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."__SDC_SHEET_ID" AS "__SDC_SHEET_ID", "PUBLIC"."TB__TAEZZB__EMPLOYEE"."__SDC_SPREADSHEET_ID" AS "__SDC_SPREADSHEET_ID" FROM "DADOSFERA_PRD_TREINAMENTOS"."PUBLIC"."TB__TAEZZB__EMPLOYEE") AS "source"
WHERE "source"."EDUCATIONFIELD" = 'Marketing'
GROUP BY "source"."GENDER"
ORDER BY "source"."GENDER" ASC
```

![dashboard](https://github.com/Pedroaguilar1232/PEDRO_ALMEIDA_DDF_SUPORTE_2023_01/blob/main/images/dash2.png).













