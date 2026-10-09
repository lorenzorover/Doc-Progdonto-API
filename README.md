# 🦷 Progdonto — Sistema Móvel de Gestão Odontológica

<p align="center">
  <img src="https://img.shields.io/badge/Versão-1.0.0-blue?style=for-the-badge&logo=android" alt="Versão 1.0" />
  <img src="https://img.shields.io/badge/Java-17-orange?style=for-the-badge&logo=java" alt="Java 17" />
  <img src="https://img.shields.io/badge/Android-SDK_34-brightgreen?style=for-the-badge&logo=android" alt="Android SDK 34" />
  <img src="https://img.shields.io/badge/Min_SDK-26_(Android_8.0)-lightgrey?style=for-the-badge" alt="Min SDK 26" />
  <img src="https://img.shields.io/badge/Status-Estável-success?style=for-the-badge" alt="Status Estável" />
</p>

---

## 📋 Sobre o Projeto

O **Progdonto** é uma solução completa desenvolvida para clínicas e consultórios odontológicos, permitindo o gerenciamento ágil, seguro e intuitivo de prontuários de pacientes, fichas clínicas, dados cadastrais e registro fotográfico de procedimentos odontológicos.

O aplicativo foi projetado para rodar em dispositivos móveis e tablets com alta performance, garantindo integridade de dados e estabilidade no consumo de memória RAM.

---

## ✨ Funcionalidades da Versão 1.0

- 👤 **Cadastro Completo de Pacientes:**
  - Registro de nome, CPF, data de nascimento, telefone, e-mail e endereço.
  - Histórico clínico pessoal e odontológico.
- 🛡️ **Validação Rigorosa de Dados:**
  - Validador matemático do dígito verificador do CPF (padrão oficial da Receita Federal).
  - Prevenção contra CPFs duplicados ou inconsistentes.
- 📸 **Gestão Segura de Fotos de Pacientes:**
  - Captura e seleção de fotos de perfil e procedimentos.
  - **Otimização de Memória (*Downsampling*):** Algoritmo de redimensionamento e amostragem de imagem no carregamento de bitmaps, impedindo vazamentos de memória (*OutOfMemoryError*) e travamentos ou zeramento de dados na tela de listagem e detalhes.
- 💾 **Persistência de Dados Confiável:**
  - Armazenamento estruturado e isolado, garantindo que o estado visual e a camada de persistência permaneçam sempre íntegros e sincronizados.

---

## 🛠️ Especificações Técnicas

| Requisito / Componente | Especificação |
| :--- | :--- |
| **Linguagem Principal** | Java 17 |
| **Plataforma** | Android OS |
| **Compile SDK** | 34 (Android 14) |
| **Target SDK** | 34 (Android 14 — Otimizado e em conformidade com a Google Play) |
| **Min SDK** | 26 (Android 8.0 Oreo — Piso mínimo de instalação) |
| **Core Library Desugaring** | Habilitado (`com.android.tools:desugar_jdk_libs:2.0.4`) para suporte a recursos modernos do Java 17 |
| **Build System** | Gradle com Android Gradle Plugin |

---

## 📱 Matriz de Compatibilidade de SDKs Android

Abaixo está a relação de compatibilidade do aplicativo com as diferentes versões do sistema Android:

| Versão do Android | Nível de API (SDK) | Status | Detalhes de Compatibilidade |
| :--- | :--- | :---: | :--- |
| **Android 15** | SDK 35 | ✅ Compatível | Funciona normalmente (retrocompatibilidade do Android) |
| **Android 14** | SDK 34 | 🎯 **Alvo Principal** | **Target SDK** (versão de referência e otimização do projeto) |
| **Android 13** | SDK 33 | ✅ Compatível | Funciona perfeitamente com controle moderno de mídia |
| **Android 12 / 12L** | SDK 31 / 32 | ✅ Compatível | Funciona perfeitamente |
| **Android 11** | SDK 30 | ✅ Compatível | Funciona perfeitamente |
| **Android 10** | SDK 29 | ✅ Compatível | Funciona perfeitamente |
| **Android 9 (Pie)** | SDK 28 | ✅ Compatível | Funciona perfeitamente |
| **Android 8.0 / 8.1 (Oreo)** | SDK 26 / 27 | 🏁 **Limite Mínimo** | **Min SDK** (versão mínima exigida para instalação) |
| **Android 7.1 ou inferior** | SDK 25 para baixo | ⛔ **Não instala** | Bloqueado pelo instalador do sistema por estar abaixo do `minSdk` |

```text
📱 Android 15 (SDK 35)      --> ✅ Funciona normalmente (o Android é retrocompatível)
📱 Android 14 (SDK 34)      --> 🎯 Alvo principal (Target SDK)
📱 Android 13 (SDK 33)      --> ✅ Funciona perfeitamente
📱 Android 12 (SDK 31/32)   --> ✅ Funciona perfeitamente
📱 Android 11 (SDK 30)      --> ✅ Funciona perfeitamente
📱 Android 10 (SDK 29)      --> ✅ Funciona perfeitamente
📱 Android 9  (SDK 28)      --> ✅ Funciona perfeitamente
📱 Android 8  (SDK 26)      --> 🏁 O limite mínimo (Min SDK)
---------------------------------------------------------------------------------
❌ Android 7 ou mais antigo (SDK 25 para baixo) --> ⛔ Não instala
```

> 💡 **Nota de Compatibilidade:** A combinação do `minSdk 26` com o `targetSdk 34` garante que o aplicativo possa ser instalado em mais de **98% de todos os aparelhos Android ativos no mercado hoje**, ao mesmo tempo em que cumpre todas as exigências de privacidade e segurança da Google Play Store.

---

## 🏗️ Arquitetura do Software

O projeto segue boas práticas de engenharia de software e separação de responsabilidades:

1. **`domain / model`:** Entidades do negócio (Paciente, Consulta, Endereço).
2. **`controller / service`:** Regras de negócio, manipulação de estado e comunicação entre camadas.
3. **`util / validators`:** Métodos utilitários e validações (CPF com cálculo de dígitos, máscaras de data/telefone e redimensionamento seguro de imagens).
4. **`database`:** Camada de persistência e acesso a dados estruturados.
5. **`ui`:** Telas e componentes visuais do Android com suporte a Material Design.

---

## 

## 🖥️ Demonstração Visual do APP

<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/01.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/02.png?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/03.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/04.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/05.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/06.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/07.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/08.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/09.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/10.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/11.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/12.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/13.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/14.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/15.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/16.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/17.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/18.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/19.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/20.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/21.jpeg?raw=true" width="300px"></img>
<img src="https://github.com/lorenzorover/Doc-Progdonto-API/blob/main/prints-progdonto/22.jpeg?raw=true" width="300px"></img>


---

## 🗺️ Roadmap de Desenvolvimento

O roadmap abaixo reúne as melhorias arquiteturais e as novas funcionalidades planejadas para as próximas versões do Progdonto:

### 🌟 Versão 1.1 — Experiência Clínica, Documentação & Backup Agendado
- [ ] 🦷 **Odontograma Clínico Interativo:**
  - Mapeamento visual gráfico da arcada dentária completa (dentes permanentes e decíduos).
  - Seleção interativa de dentes para anotação de cáries, restaurações, próteses, tratamentos de canal e extrações.
- [ ] 📄 **Geração e Exportação de PDF:**
  - Emissão automática do Termo de Consentimento Livre e Esclarecido (TCLE).
  - Exportação de ficha completa do paciente e histórico clínico para impressão ou compartilhamento em PDF.
- [ ] ☁️ **Backup Automático Programável (Estilo WhatsApp):**
  - Rotina de backup automático de dados e fotos em segundo plano.
  - Configuração personalizada pelo usuário de **intervalo** (diário, semanal ou mensal).
  - Definição do **dia da semana** e do **horário específico** para execução automática (ex: todo domingo às 03:00).
  - Botão de backup manual sob demanda e restauração rápida de dados.

### 🌟 Versão 2.0 — Novo Banco de Dados de Alta Segurança & Sistema de Login
- [ ] 🛡️ **Migração para Banco de Dados Dedicado de Alta Segurança:**
  - Implementação de um banco de dados relacional robusto, com criptografia de ponta a ponta e alta integridade transacional.
  - **Substituição do backup de dados do Google:** O antigo modelo de backup avulso é substituído por essa base de dados segura e centralizada, garantindo maior blindagem e sincronismo.
- [ ] 🔐 **Sistema de Autenticação com Perfis Distintos (RBAC):**
  - Telas e níveis de login com acessos diferenciados para cada função na clínica (ex: Administrador, Cirurgião-Dentista, Recepcionista/Secretária).
  - Restrição de visualização de dados sigilosos e registro de auditoria por usuário.
- [ ] 🧩 **Refatoração com Interfaces para Regras de Negócio:**
  - Implementação de interfaces desacopladas para validadores e regras de negócio de pacientes (padrão *Strategy / Clean Architecture*), facilitando testes unitários e modularidade.

---

<p align="center">
  Desenvolvido com foco em desempenho, estabilidade e usabilidade clínica. 🩺✨
</p>
