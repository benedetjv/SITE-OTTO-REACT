# Dr. Otto Beckedorff – Ortopedia & Tratamento da Dor (React SPA)

## 💻 Visão Geral do Projeto

Este repositório contém o código-fonte do site profissional do Dr. Otto Beckedorff, desenvolvido como uma **Single Page Application (SPA)** usando React e o empacotador Vite.

O projeto foi estruturado para separar o conteúdo estático (textos, telefones, links) da lógica de apresentação (componentes React), tornando a manutenção rápida e segura.

## 🚀 Tecnologias Utilizadas

* **Frontend:** React (com JSX)
* **Empacotador/Build:** Vite
* **Estilização:** Bootstrap 5.3.x e CSS Customizado
* **Versionamento:** Git & GitHub Actions

## ⚙️ Configuração e Desenvolvimento Local

Para realizar qualquer alteração no código e testá-la antes do deploy, siga estes passos:

### 1. Instalação das Dependências

Na pasta raiz do projeto, instale todas as dependências (Bootstrap, React, etc.):

```bash
npm install




####

2. Executando o Servidor de Desenvolvimento
Para rodar o site localmente em modo de desenvolvimento (com recarregamento automático):

✍️ Guia de Alterações e Manutenção (Maneira Correta)
1. Alterar Textos, Telefones ou Links (Recomendado!)
NUNCA altere textos diretamente nos arquivos .jsx!

Todas as informações textuais, links de menu, detalhes de serviços, endereços e telefones de contato devem ser alterados exclusivamente no arquivo de conteúdo central:

➡️ Arquivo: src/content.js

Edite as propriedades dentro do objeto siteContent (ex: siteContent.contato.clinicas[0].telefone). Suas alterações serão refletidas automaticamente no site.

2. Alterar Estilos e Layout
A. Estilos (Cores, Fontes, Responsividade)
➡️ Arquivo: css/styles.css

Este arquivo contém todas as regras CSS personalizadas. Se precisar ajustar margens, cores (usando as variáveis CSS definidas no bloco :root), ou a responsividade (@media queries), edite este arquivo.

B. Componentes e Estrutura (Avançado)
➡️ Pasta: src/components/

Se precisar adicionar uma nova seção, reorganizar o layout de uma seção existente (ex: Hero), ou mudar a ordem dos componentes, você deve editar os arquivos .jsx correspondentes e atualizar o src/App.jsx.

3. Correção de Imagens (Recomendação de Performance)
Rotação de Imagens: Se a imagem do Hero (foto-otto.jpg) voltar a aparecer de lado, significa que a orientação EXIF original do arquivo precisa ser corrigida. A solução ideal é editar e salvar o arquivo no formato vertical correto, e fazer um novo commit. (Uma correção temporária via CSS foi adicionada em css/styles.css, mas a correção do arquivo é preferível.)

Otimização: O site já está configurado para usar o formato WEBP e Lazy Loading nas principais imagens, o que é crucial para a velocidade em dispositivos móveis. Mantenha essa estrutura de <picture> ao substituir qualquer imagem.
