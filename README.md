# 🐾 PataAmiga

Plataforma web e mobile que conecta ONGs e pessoas que querem doar animais, quem encontrou um animal perdido, quem quer adotar e quem perdeu o seu bichinho, sempre com foco em adoção responsável e em facilitar doações para ONGs.

---

## 📑 Sumário
- [1. Sobre o Projeto](#1-sobre-o-projeto)
  - [O Problema](#o-problema)
  - [A Solução](#a-solução)
  - [Objetivos](#objetivos)
  - [Público-alvo](#público-alvo)
  - [Adoção Responsável](#adoção-responsável-princípios-do-projeto)
  - [Requisitos Funcionais e Não Funcionais](#requisitos-do-sistema)
- [2. Tecnologias, Ferramentas e Infraestrutura](#2-tecnologias-ferramentas-e-infraestrutura)
  - [Arquitetura](#visão-geral-da-arquitetura)
  - [Stack Tecnológica](#stack-tecnológica)
  - [Infraestrutura e DevOps](#infraestrutura-e-devops)
- [3. Metodologias Utilizadas](#3-metodologias-utilizadas)
  - [Metodologia de Desenvolvimento](#31-qual-metodologia-e-por-quê)
  - [Aplicação do Scrum](#32-como-o-scrum-será-aplicado)
  - [Uso do Git e GitHub](#33-como-o-git-e-o-github-serão-usados)
- [4. Projeto de Interface](#4-projeto-de-interface)
- [5. Modelagem do Sistema](#5-modelagem-do-sistema)
- [6. Planejamento](#6-planejamento)
- [7. Estrutura do Repositório](#7-estrutura-do-repositório)

---

## 1. Sobre o Projeto

### O Problema
Todos os dias animais são abandonados, se perdem ou ficam esperando um lar em ONGs que já estão superlotadas e com poucos recursos. Ao mesmo tempo, muitas pessoas querem adotar, mas não sabem onde procurar. Quem perde um animal, ou encontra um na rua, também costuma depender de grupos de redes sociais, onde as informações se perdem rápido.

### A Solução
O **PataAmiga** é um sistema que reúne tudo em um só lugar:
- **🐶 Adoção:** ONGs e pessoas publicam animais disponíveis com fotos e informações completas (espécie, porte, idade, temperamento, vacinas, castração, histórico de saúde, cidade).
- **🔍 Animais perdidos e encontrados:** Quem perdeu ou encontrou um animal publica a ocorrência com foto, local e data. O sistema cruza os dados e avisa usuários próximos.
- **💚 Doações para ONGs:** Cada ONG verificada tem um perfil com suas necessidades (ração, medicamentos, castração, lar temporário) e pode receber doações via Pix, direto na conta dela.
- **🤝 Adoção responsável:** A plataforma estimula a adoção consciente, com triagem, termo de compromisso e acompanhamento pós-adoção.

### Objetivos
- Reduzir o tempo de permanência dos animais em abrigos e ONGs.
- Aumentar as chances de reencontro entre animais perdidos e seus tutores.
- Facilitar o recebimento de doações e voluntariado pelas ONGs.
- Combater o abandono, a devolução de animais e a comercialização irregular.

### Público-alvo

| Perfil | O que faz na plataforma |
| :--- | :--- |
| **Adotante** | Busca animais, preenche o questionário de adoção, acompanha o processo |
| **Doador de animal / Tutor** | Publica animal para adoção (com triagem e termo de responsabilidade) |
| **ONG** | Perfil verificado, gerencia animais, recebe doações e solicitações de adoção |
| **Quem encontrou um animal** | Registra o animal encontrado e conversa com possíveis tutores |
| **Quem perdeu um animal** | Registra o disappearance e recebe alertas de animais encontrados |
| **Doador financeiro / Voluntário** | Doa para ONGs, oferece lar temporário ou ajuda em eventos |
| **Administrador** | Verifica ONGs, modera publicações e trata denúncias |

### Adoção responsável (princípios do projeto)
1. **Proibida a venda de animais:** Anúncios com preço, "taxa de reserva" suspeita ou indícios de criação comercial são bloqueados e denunciáveis.
2. **Questionário de adoção:** Analisado pela ONG ou pelo doador antes de qualquer entrega.
3. **Termo de responsabilidade digital:** Aceito pelo adotante, com compromisso de vacinação, castração, não abandono e devolução caso não possa mais cuidar.
4. **Acompanhamento pós-adoção:** Lembretes automáticos após 7, 30 e 90 dias para atualização do animal.
5. **Animais encontrados:** A entrega ao suposto tutor exige comprovação de posse.
6. **Verificação das ONGs:** Cadastro com CNPJ, documentos e aprovação manual antes do selo de "ONG verificada".
7. **Privacidade:** O endereço exato de quem encontrou o animal não é exibido publicamente (apenas região aproximada).

### Requisitos do Sistema

<details>
<summary><b>Clique para ver os Requisitos Funcionais (RF) e Não Funcionais (RNF)</b></summary>

#### Requisitos Funcionais (RF)
- **RF01** – Cadastro e login de usuários (e-mail e Google), com perfis diferentes.
- **RF02** – Cadastro de ONGs com envio de documentos e verificação pelo administrador.
- **RF03** – Publicar animal para adoção com várias fotos e ficha completa.
- **RF04** – Buscar e filtrar animais (espécie, porte, idade, sexo, cidade, ONG, castrado, vacinado).
- **RF05** – Registrar animal perdido e encontrado com foto, local e data.
- **RF06** – Mapa com ocorrências de animais perdidos e encontrados.
- **RF07** – Alertas por região e sugestão de possíveis correspondências.
- **RF08** – Questionário de adoção e fluxo de aprovação.
- **RF09** – Termo de responsabilidade digital.
- **RF10** – Chat interno entre as partes.
- **RF11** – Doação via Pix para ONGs com transparência.
- **RF12** – Campanhas de ONGs com meta e barra de progresso.
- **RF13** – Acompanhamento pós-adoção com lembretes.
- **RF14** – Denúncia de anúncios suspeitos e moderação.
- **RF15** – Favoritar animais e receber notificações.
- **RF16** – Compartilhar o anúncio em redes sociais.

#### Requisitos Não Funcionais (RNF)
- **RNF01** – Responsivo e funcional em celulares simples (PWA).
- **RNF02** – Conformidade com a LGPD.
- **RNF03** – Fotos otimizadas automaticamente.
- **RNF04** – Autenticação segura (JWT, senhas criptografadas).
- **RNF05** – Disponibilidade mínima de 99% e backups diários.
- **RNF06** – Acessibilidade (WCAG 2.1 nível AA).
- **RNF07** – Tempo de carregamento inferior a 3 segundos em 4G.

</details>

---

## 2. Tecnologias, Ferramentas e Infraestrutura

### Visão geral da arquitetura

```mermaid
flowchart LR
    U[Usuário<br/>Web / Mobile PWA] --> CDN[CDN + WAF]
    CDN --> FE[Front-end<br/>React + Next.js]
    FE --> API[API REST<br/>NestJS - Node.js]
    API --> DB[(PostgreSQL<br/>+ PostGIS)]
    API --> CACHE[(Redis<br/>cache e filas)]
    API --> S3[(Armazenamento<br/>de imagens)]
    API --> PIX[Gateway de pagamento<br/>Pix]
    API --> MAIL[E-mail / Push<br/>notificações]
    API --> MAP[API de mapas]
    API --> OBS[Logs e monitoramento]
