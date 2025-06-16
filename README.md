# Clinica-M-dica---SI-POO
Site para navegação de sistema de cadastro de clientes e médicos, e navegação às informações da clínica - Trabalho final POO - Sistemas de Informação PUC Minas

# Sistema de Gerenciamento de Clínica Médica: Clínica Vida

[cite_start]Este projeto é uma aplicação de console desenvolvida em C# que simula as operações básicas de gerenciamento de pacientes, médicos e agendamento de consultas.  [cite_start]O sistema permite o cadastro, listagem, edição, exclusão e busca de informações sobre pacientes e médicos, além de funcionalidades para agendamento, listagem, edição, cancelamento e busca de consultas.  O sistema também inclui relatórios básicos e filtragens. [cite_start]Os dados são persistidos em arquivos JSON. 

## Funcionalidades Principais

### Gestão de Pacientes
* [cite_start]Cadastrar novos pacientes com nome, CPF, data de nascimento, telefone, email e histórico médico. 
* [cite_start]Listar todos os pacientes cadastrados. 
* Editar informações de pacientes existentes.
* [cite_start]Excluir pacientes do sistema. 
* [cite_start]Buscar pacientes por nome ou CPF. 
* [cite_start]Visualizar histórico de consultas de um paciente. 

### Gestão de Médicos
* [cite_start]Cadastrar novos médicos com nome, CPF, data de nascimento, telefone, email, especialidade e CRM. 
* [cite_start]Listar todos os médicos cadastrados. 
* Editar informações de médicos existentes.
* [cite_start]Excluir médicos do sistema. 
* [cite_start]Buscar médicos por nome, CRM ou especialidade. 
* [cite_start]Filtrar médicos por especialidade. 

### Gestão de Consultas
* [cite_start]Agendar novas consultas, associando um paciente, um médico e uma data/hora. 
* [cite_start]Validar agendamentos (data no futuro, paciente não ter mais de uma consulta com o mesmo médico no dia, médico com no máximo 10 consultas no dia, médico sem consultas no mesmo horário). 
* [cite_start]Listar todas as consultas agendadas. 
* [cite_start]Editar informações de consultas (data/hora, observações, status). 
* [cite_start]Cancelar consultas. 
* [cite_start]Registrar atendimento de uma consulta, adicionando prontuário, diagnóstico e prescrições. 
* [cite_start]Buscar consultas por paciente, médico ou data. 
* [cite_start]Gerar relatório de total de consultas por médico. 
* [cite_start]Listar consultas específicas de um médico. 

## Estrutura do Projeto

[cite_start]O sistema segue uma arquitetura simples, orientada a objetos, comum para aplicações de console de pequeno porte.  [cite_start]Ele é estruturado em classes que representam as entidades do domínio (`Pessoa`, `Paciente`, `Medico`, `Consulta`) e uma classe principal (`Program`) que gerencia a lógica de negócio, a interação com o usuário (menu e entradas/saídas) e a persistência de dados. 

* `Pessoa.cs`: Classe base abstrata para entidades com dados comuns.
* `Paciente.cs`: Classe que representa um paciente, herda de `Pessoa`.
* `Medico.cs`: Classe que representa um médico, herda de `Pessoa`.
* `Consulta.cs`: Classe que representa uma consulta, relacionando `Paciente` e `Medico`.
* `Program.cs`: Contém a lógica principal da aplicação, menu de interação, gerenciamento das operações e persistência de dados.
* `pacientes.json`, `medicos.json`, `consultas.json`: Arquivos JSON utilizados para a persistência dos dados do sistema.
* `docs/diagrama_classes.md`: Contém o código Mermaid para o diagrama de classes UML do sistema.

## Como Compilar e Executar

Este projeto pode ser compilado e executado utilizando o .NET SDK.

### Pré-requisitos

Certifique-se de ter o [.NET SDK](https://dotnet.microsoft.com/download) instalado em sua máquina (versão 6.0 ou superior recomendada).

### Compilação

1.  **Navegue até a raiz do projeto:**
    Abra o terminal (Prompt de Comando, PowerShell ou Bash) e navegue até o diretório onde os arquivos `.cs` do projeto estão localizados (onde está o arquivo `.csproj` do seu projeto). Exemplo:
    ```bash
    cd C:\Caminho\Para\SeuProjeto\ClinicaVida
    ```
    *Substitua `C:\Caminho\Para\SeuProjeto\ClinicaVida` pelo caminho real da pasta do seu projeto.*

2.  **Restaure as dependências (se necessário):**
    ```bash
    dotnet restore
    ```

3.  **Compile o projeto:**
    ```bash
    dotnet build
    ```
    Isso criará os arquivos executáveis na pasta `bin/Debug/netX.Y/` (onde `X.Y` é a versão do .NET target do seu projeto).

### Execução

Após a compilação bem-sucedida:

1.  **Execute a aplicação:**
    ```bash
    dotnet run
    ```
    Ou, se você já compilou e está na pasta de saída da compilação:
    ```bash
    .\ClinicaVida.exe  # No Windows
    ./ClinicaVida     # No Linux/macOS
    ```
    *(Substitua `ClinicaVida` pelo nome real do executável gerado, que geralmente corresponde ao nome do seu arquivo `.csproj`)*

2.  O menu da aplicação de console será exibido, permitindo que você interaja com o sistema.

## Documentação Completa

A documentação detalhada do projeto, incluindo a descrição detalhada, arquitetura do sistema, diagrama de classes e padrões de projeto utilizados, está disponível no arquivo:

* `DESCRIÇÃO PROJETO - CLÍNICA VIDA.pdf`
