# skia.md

## Visão Geral

Este documento oferece uma visão detalhada sobre a biblioteca Skia e os fundamentos da arquitetura mobile, abordando aspectos de hardware, software, redes e boas práticas para desenvolvimento de aplicativos móveis.

---

## Skia

### O que é?
Skia é uma biblioteca de gráficos 2D de código aberto desenvolvida pelo Google. Ela permite renderização de alta performance e multiplataforma, sendo usada em produtos como Google Chrome, Chrome OS, Android e Flutter.

### Características
- **Código Aberto**: Disponível para uso comercial e não comercial.
- **Linguagem**: Escrita em C++, com alto desempenho.
- **Multiplataforma**: Abstrai APIs gráficas como OpenGL, Vulkan, DirectX e Metal.
- **Renderização Avançada**: Suporte a texto, imagens, formas e transformações gráficas.
- **Desempenho**: Suporte à aceleração por hardware e renderização eficiente com GPU.

### Uso com OpenGL
- **Aceleração de hardware**: Usa OpenGL para melhorar a performance.
- **Portabilidade**: Pode alternar entre OpenGL, Vulkan, Metal, etc., conforme a plataforma.

### Skia e Flutter
- **Motor de Renderização**: Skia é usado para desenhar a interface do Flutter.
- **Consistência entre plataformas**: Permite que a UI Flutter seja idêntica em Android, iOS e web.
- **Alternativa**: O Flutter 3.10 introduziu o Impeller como novo motor padrão em iOS e experimental no Android.
- **Web**: Flutter usa Skia via `canvaskit` e `skwasm` para renderização no navegador.

---

## Arquitetura Mobile

### O que é?
A arquitetura mobile define a estrutura e a organização dos componentes de um app, como interface, lógica de negócios, APIs e bancos de dados, visando eficiência, escalabilidade e manutenção.

### Principais Aspectos
- **Estruturação e organização**: Divisão clara entre UI, lógica de negócios e dados.
- **Escalabilidade e manutenção**: Suporte à evolução do app com facilidade de manutenção.
- **Desempenho e testabilidade**: Reduz uso de recursos e facilita testes automatizados.

### Considerações
- Escolha da arquitetura adequada (MVC, MVP, MVVM, Clean Architecture).
- Experiência do usuário intuitiva e responsiva.
- Segurança, otimização de desempenho, suporte a múltiplos dispositivos.

### Padrões Comuns
- **MVC**: Modelo, Visão e Controlador.
- **MVP**: Presenter atua entre View e Model.
- **MVVM**: ViewModel faz binding entre a View e o Model.
- **Clean Architecture**: Separação total entre domínios, independente de frameworks.
- **MVI**: Fluxo de dados unidirecional, foco em gerenciamento de estado.

---

## Arquitetura de Hardware Mobile

### Definição
Estrutura física dos dispositivos móveis, incluindo CPU, GPU, RAM, sensores, barramentos e mais.

### Componentes
- **CPU**: Executa instruções e lógica principal.
- **GPU**: Processa gráficos e imagens.
- **RAM e Armazenamento**: Dados temporários e permanentes.
- **Tela e Sensores**: Interação com o usuário e o ambiente.

### Arquiteturas Comuns
- **ARM**: Eficiência energética e desempenho.
- **x86**: Alta performance, comum em desktops e alguns tablets.

### Importância
A arquitetura de hardware influencia diretamente no desempenho, consumo de energia e experiência geral do usuário.

---

## Arquitetura de Rede Mobile

### Definição
Organização da infraestrutura de comunicação entre dispositivos móveis e redes externas.

### Componentes
- **Estação Móvel (MS)**: Dispositivo do usuário.
- **RAN (Rede de Acesso Rádio)**: Torres e infraestrutura sem fio.
- **Core Network**: Gerencia tráfego e autenticação.
- **Bancos de Dados**: Informações sobre os usuários e conexões.

### Tecnologias
- **2G/3G (GSM, UMTS)**
- **4G (LTE)**
- **5G**

### Função
Viabilizar chamadas, mensagens, internet e serviços em tempo real em dispositivos móveis.

---

## Conclusão

Skia é uma biblioteca essencial para renderização gráfica multiplataforma e tem papel central no ecossistema Flutter. Já a arquitetura mobile — composta pelas vertentes de software, hardware e rede — é fundamental para garantir que aplicativos sejam eficientes, escaláveis, seguros e compatíveis com as expectativas modernas de desempenho e usabilidade.