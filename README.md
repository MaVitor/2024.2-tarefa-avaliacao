# 2024.2 Avaliação do 1o período de Sistemas Operacionais

## Informações gerais
- **Objetivo do repositório**: Avaliação do 1o bimestre da Disciplina de sistemas operacionais do curso de TADS do IFRN-CNAT
- **Público alvo**: alunos da disciplina de SO (Sistemas Operacionais) do curso de TADS (Superior em Tecnologia em Análise e Desenvolvimento de Sistemas) no CNAT-IFRN (Instituto Federal de Educação, Ciência e Tecnologia do Rio Grande do Norte - Campus Natal-Central).
- **Disciplina**: **SO** Sistemas Operacionais
- **Professor**: [Leonardo A. Minora](https://github.com/leonardo-minora)
- **Aluno**: Mateus Vitor Cavalcanti Rodrigues
- **Matrícula**: 20232014040031

---

## Questão 1. Introdução a Sistemas Operacionais

**Pergunta:**  
Considere as funções e objetivos principais de um sistema operacional conforme discutido no texto. Explique como um sistema operacional gerencia os recursos de hardware e software de um computador para garantir eficiência e segurança. Em sua resposta, aborde os seguintes pontos:

- Gerenciamento de processos  
- Gerenciamento de memória  
- Gerenciamento de dispositivos de entrada e saída  
- Gerenciamento de arquivos  

**Resposta:**  

1. **Gerenciamento de Processos:**  
   O sistema operacional gerencia os processos em execução, garantindo que múltiplos programas possam ser executados simultaneamente. Ele utiliza técnicas como escalonamento para distribuir tempo de CPU, e isolamento para evitar interferências entre processos.  
   **Exemplo prático:** Quando abrimos várias abas no navegador, o sistema operacional aloca recursos de CPU para cada aba, evitando que uma aba com um erro feche todas as outras.  

2. **Gerenciamento de Memória:**  
   O sistema operacional aloca e monitora o uso de memória pelos processos. Ele utiliza a memória virtual para otimizar o uso da RAM e evitar conflitos entre os processos.  
   **Exemplo prático:** Ao abrir um editor de texto e uma planilha, o sistema operacional aloca memória suficiente para cada programa funcionar sem ocupar o espaço um do outro.  

3. **Gerenciamento de Dispositivos de Entrada e Saída:**  
   O sistema operacional fornece interfaces para dispositivos como teclado, mouse, disco rígido e impressoras, organizando filas e gerenciando acessos.  
   **Exemplo prático:** Ao conectar um pendrive, o sistema detecta automaticamente o dispositivo, disponibilizando o acesso aos arquivos nele contidos.  

4. **Gerenciamento de Arquivos:**  
   O sistema organiza, armazena e recupera arquivos, utilizando sistemas de arquivos como FAT32 ou NTFS para gerenciar permissões, hierarquias e acessos.  
   **Exemplo prático:** Ao salvar um documento no computador, o sistema operacional organiza o arquivo no disco, permitindo sua recuperação posterior.

---

## Questão 2. Estrutura de Sistemas Operacionais

**Pergunta:**  
Com base no texto sobre a estrutura de sistemas operacionais, analise como as diferentes arquiteturas (monolítica, microkernel e camadas) impactam o custo com a equipe de desenvolvimento e a segurança do sistema operacional. Em sua resposta, considere os seguintes pontos:

- Complexidade de implementação e manutenção  
- Necessidade de especialização da equipe  
- Potenciais vulnerabilidades de segurança  
- Facilidade de atualização e correção de falhas  

**Resposta:**  

| Arquitetura      | Complexidade de Implementação | Necessidade de Especialização | Vulnerabilidades de Segurança          | Facilidade de Atualização            |
|-------------------|-------------------------------|--------------------------------|----------------------------------------|---------------------------------------|
| **Monolítica**   | Baixa                         | Menor                          | Alta, devido à integração do código   | Difícil, pois mudanças afetam todo o sistema |
| **Microkernel**  | Alta                          | Maior                          | Baixa, graças ao isolamento dos módulos | Fácil, pois atualizações são isoladas |
| **Camadas**      | Moderada                      | Moderada                       | Moderada, com riscos na comunicação entre camadas | Moderada, dependendo da camada afetada |

**Exemplo prático:**  
- **Monolítica:** O Linux tradicional é monolítico, mas sua modularidade ajuda a gerenciar partes do sistema.  
- **Microkernel:** O Minix usa essa arquitetura, com o kernel responsável apenas por funções básicas, aumentando a segurança.  
- **Camadas:** O THE (Teaching OS) foi um exemplo clássico de sistema em camadas, onde cada nível executa funções específicas.

---

## Questão 3. Introdução à Segurança de Sistemas Operacionais

**Pergunta:**  
Considerando os mecanismos de segurança discutidos, analise como a implementação de controles de acesso e criptografia pode impactar a performance e a usabilidade de um sistema operacional. Em sua resposta, aborde os seguintes pontos:

- Benefícios e desafios de cada mecanismo  
- Impacto na experiência do usuário  
- Exemplos de situações onde esses mecanismos são críticos  

**Resposta:**  

1. **Controle de Acesso:**  
   - **Benefícios:** Impede acessos não autorizados e garante a confidencialidade.  
   - **Desafios:** Pode dificultar o uso se exigir autenticação frequente.  
   - **Impacto na experiência:** Processos adicionais como autenticação por senha ou biometria podem ser inconvenientes.  
   **Exemplo:** Ao acessar um servidor remoto, o controle de acesso impede que usuários não autorizados entrem no sistema.  

2. **Criptografia:**  
   - **Benefícios:** Garante a segurança de dados em trânsito e armazenados.  
   - **Desafios:** Consome recursos computacionais, reduzindo a performance.  
   - **Impacto na experiência:** Processos mais lentos podem ocorrer ao transferir arquivos grandes.  
   **Exemplo:** Ao enviar dados bancários via internet, a criptografia impede que informações sejam interceptadas.  

---

## Questão 4. Custo de Processamento versus Algoritmo Ótimo de Escalonamento

**Pergunta:**  
Considere os conceitos de custo de processamento e algoritmo ótimo de escalonamento. Analise como diferentes algoritmos de escalonamento podem impactar a performance de um sistema operacional em termos de tempo de resposta, tempo de espera e utilização do processador.  

**Resposta:**  

| Algoritmo       | Vantagens                                           | Desvantagens                                         | Situação Ideal                                      |
|------------------|----------------------------------------------------|----------------------------------------------------|---------------------------------------------------|
| **FCFS**        | Simples de implementar                             | Pode causar o problema de "convoy effect"          | Uso em sistemas onde a ordem é mais importante que a velocidade |
| **Round Robin** | Justo, todos os processos têm tempos iguais         | Overhead elevado devido à troca de contexto        | Sistemas interativos, como terminais de usuário   |

**Exemplo prático:**  
- **FCFS:** Processamento de tarefas na fila de uma impressora.  
- **Round Robin:** Uso em servidores compartilhados para atender múltiplos clientes.

---

## Questão 5. Aplicativo em Python vs Aplicativos em C

**Pergunta:**  
Explique o caminho que as instruções seguem desde um aplicativo escrito em Python e um aplicativo escrito em linguagem C até serem executadas pelo hardware.  

**Resposta:**  

| Etapa                | Python                                   | C                                       |
|----------------------|------------------------------------------|-----------------------------------------|
| **Tradução**         | Interpretado (em tempo de execução)      | Compilado (transformado em binário)     |
| **Velocidade**       | Mais lento devido à interpretação        | Mais rápido, já executa código binário  |
| **Kernel/Drivers**   | Ambos interagem com kernel e drivers para acesso ao hardware | Ambos interagem com kernel e drivers para acesso ao hardware |

**Exemplo prático:**  
- **Python:** Um script para automação de tarefas.  
- **C:** Desenvolvimento de sistemas embarcados que exigem alta performance.

