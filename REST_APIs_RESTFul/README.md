# REST API's RESTFul do 0 à Azure com ASP.NET Core 5 e Docker

Este curso aborda a criação de uma API RESTFul do 0 absoluto até o deploy na Azure com a utilização do Docker e o consumo da mesma API utilizando React JS.

## Fundamentos Teóricos do REST

### O que são Webservices

Web-services são aplicações interoperáveis hospedadas e acessadas através da web por meio do protocolo HTTP. Diferente de websites que visam a visualização por humanos, os web-services são direcionados para outros programas. Eles possibilitam a interoperabilidade entre softwares e aplicações executando em diferentes plataformas e frameworks, permitindo a execução de operações complexas por meio da combinação de serviços de forma baixamente acoplada. De acordo com o World Wide Web Consortium (W3C), os web-services são aplicações cliente servidor que se comunicam pela World Wide Web's (WWW) através do protocolo HTTP.

### Desenvolvimento de software antes do REST

Quando os softwares deixaram de ser exclusividade apenas de órgãos do governo, e as empresas começaram a utilizá-los em suas operações, e com o tempo, diferentes setores precisavam integrar seus sistemas de maneira que, por exemplo, o Departamento Pessoal precisasse acessar dados do Jurídico, ou o departamento de Fiscal precisasse acessar dados do Vendas.
Com essa necessidade, as empresas desenvolveram diferentes "padrões" para solucionar este problema, como: RMI, SOAP, Corba, DCE, DCOM, etc. E esses diferentes padrões acabaram gerando muitos problemas, como por exemplo a má interoperabilidade entre esses diferentes sistemas, e o fato dos clientes ficarem atrelados a um fornecedor específico, como por exemplo: se sua empresa comprasse um software da Oracle, ele ficava "preso" à esse sistema e seu padrão específico.
Com o passar do tempo, dois desses padrões se sobressaíram: SOAP e REST.

### SOAP (Simples Object Access Protocol)

O protocolo SOAP foi criado pela Microsoft em 1998 e é utilizado para troca de informações entre aplicações em ambientes distribuídos. Ele define um formato padrão baseado em XML para a estruturação de mensagens, permitindo interoperabilidade entre diferentes plataformas e tecnologias. As mensagens SOAP são compostas por um envelope XML que contém informações sobre o remetente, o destinatário e o conteúdo da mensagem, com um cabeçalho opcional e um corpo que contém os dados da mensagem. O protocolo SOAP é frequentemente usado em conjunto com o HTTP para permitir a comunicação entre aplicações e é amplamente utilizado em serviços web.

### REST (Representational State Transfer)

Representational State Transfer (REST) é um estilo de arquitetura de software para sistemas distribuídos de hipermídia, como a World Wide Web. O REST é baseado em 6 restrições:

| SOAP | REST |
| :---: | :---: |
| Protocolo de troca de mensagens em XML | Estilo Arquitetural |
| Usa WSDL na comunicação entre cliente e servidor | Usa XML, JSON, YAML, etc. para enviar e receber dados|
| Invoca serviços através de chamadas de método RPC | Simplesmente chama serviços via URL PATH |
| Não retorna um resultado facilmente legível para humanos | Resultado legível por humanos já que é simplesmente JSON, XML, YAML, etc. em seu estado bruto |
| Comunicação feita HTTP mas pode usar outros protocolos como SMTP, FTP, etc. | Comunicação feita unicamente por HTTP |
| JavaScript pode invocar um serviço SOAP mas essa implementação é bastante complexa de se fazer | Fácil de invocar via JavaScript |
| Comparado com REST sua performance não é das melhores | Comparado com SOAP a performance é melhor, consome menos recursos de processamento, o código é mais enxuto, etc. |
