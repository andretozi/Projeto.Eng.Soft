# Plataforma de Documentação Inteligente de Projetos de Engenharia de Software

## Sobre o Projeto
A documentação de software é frequentemente negligenciada devido à velocidade das entregas ágeis. Para resolver este problema, esta plataforma centraliza e conecta repositórios de código-fonte (GitHub), diagramas e arquivos diversos, gerando artefatos de documentação de forma automatizada. 

O grande diferencial técnico da solução consiste na aplicação de Inteligência Artificial Generativa (LLMs) para interpretar o código, commits e arquivos isolados, diminuindo o esforço manual de engenheiros e gestores. A arquitetura do sistema baseia-se na integração de múltiplos microsserviços robustos.

## Foco deste Repositório: Módulo de Ingestão e Gerenciamento de Dados
Este repositório contém o código-fonte referente ao módulo de "Upload, Cadastro e Gerenciamento de Dados (Ingestão)", responsável por alimentar a plataforma com as informações necessárias para a geração de documentação. 

As principais funcionalidades deste módulo incluem:
* **Integração com Controle de Versão:** Realiza a conexão com o GitHub para a leitura contínua de repositórios, branches e pull requests.
* **Ingestão de Arquivos:** Permite o upload de arquivos variados inerentes ao ciclo de desenvolvimento, como PDFs de requisitos, atas de reunião, diagramas legados e desenhos de telas.
* **Estruturação de Dados:** Garante a organização das informações separadas por projetos, estruturadas em diretórios e classificadas por tipos de documentos. Também é responsável por organizar os artefatos gerados na plataforma.
* **Automação via Inteligência Artificial:** O módulo utiliza IA para a classificação automática dos documentos enviados e para a extração de metadados estruturados. A IA é capaz, por exemplo, de identificar que um arquivo PDF corresponde a uma "Especificação de Requisitos" e realizar o vínculo automático deste documento ao trecho de código-fonte relevante.

## Visão Geral do Ecossistema
Este microsserviço de Ingestão atua em conjunto com outros módulos do sistema para compor a plataforma final. O ecossistema abrange os seguintes microsserviços adicionais:
* **Gerenciamento de Projetos e Usuários:** Controle de acesso (RBAC) e gestão de equipes.
* **Módulo de Relatórios:** Geração de documentos textuais (PDF, Markdown, DOCX).
* **Módulo de Apresentações:** Criação automatizada de slides para reuniões de acompanhamento.
* **Módulo de Diagramas e Documentos Técnicos:** Engenharia reversa visual baseada na análise do código.
* **Módulo de Consulta:** Chat alimentado por IA para responder a perguntas técnicas com base nos materiais do projeto.

## Perfis de Usuário
A plataforma foi desenhada para atender às seguintes necessidades:
* **Tech Lead / Arquiteto:** Utiliza a plataforma para gerar diagramas de arquitetura atualizados e realizar a auditoria da documentação técnica sem a necessidade de construí-los manualmente.
* **Gerente de Projetos (PM):** Emprega a ferramenta para extrair resumos de sprints e criar apresentações de status direcionadas à diretoria e aos clientes.
* **Desenvolvedor:** Acessa a documentação técnica para compreender módulos legados e integra os seus repositórios para garantir que a base de conhecimento permaneça "viva".

## Tecnologias Utilizadas
*(Preencha com a stack técnica definida pela sua equipe)*
* **Linguagem / Framework Backend:** [Ex: Java/Spring Boot, Python/FastAPI, Node.js/NestJS]
* **Banco de Dados:** [Ex: PostgreSQL, Oracle APEX, MongoDB]
* **Integração de IA:** [Ex: API do OpenAI, Google Gemini, Framework LangChain]
* **Infraestrutura / Mensageria:** [Ex: Docker, Kubernetes, RabbitMQ]

## Como Executar o Projeto Localmente
*(Adapte as instruções de acordo com o ambiente da sua equipe)*

1. Realize o clone deste repositório: `git clone https://github.com/seu-usuario/seu-repo.git`
2. Acesse o diretório do projeto e instale as dependências: `npm install` ou `pip install -r requirements.txt`
3. Configure as credenciais de banco de dados e chaves de API no arquivo `.env` (utilize o `.env.example` como base).
4. Inicialize o serviço de Ingestão de Dados: `npm run dev` ou equivalente.

---
Projeto acadêmico desenvolvido para a disciplina de Projeto de Engenharia de Software com Microsserviços, Universidade Presbiteriana Mackenzie.
