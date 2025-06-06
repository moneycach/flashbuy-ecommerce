# FlashBuy E-commerce

Este repositório contém o código-fonte do aplicativo FlashBuy E-commerce, que inclui um aplicativo Android e uma aplicação web administrativa.

## Estrutura do Projeto

- `app/` - Aplicativo Android FlashBuy
- `web-admin/` - Aplicação web administrativa

## Requisitos

### Aplicativo Android
- Android Studio Arctic Fox (2021.3.1) ou superior
- JDK 17
- Gradle 8.1.0 ou superior
- Dispositivo/Emulador com Android 8.0 (API 26) ou superior

### Aplicação Web
- Node.js 18.x ou superior
- npm 9.x ou superior
- MongoDB 6.0 ou superior

## Configuração e Execução

### Aplicativo Android

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/flashbuy-ecommerce.git
   cd flashbuy-ecommerce
   ```

2. Abra o projeto no Android Studio.

3. Configure as chaves de API no arquivo `local.properties`:
   ```properties
   GOOGLE_MAPS_API_KEY=AIzaSyB7jewrMHxjKNMtCYwNOPSAVh8IF2dc_W4
   STRIPE_PUBLISHABLE_KEY=sua_chave_publica_do_stripe
   ```

4. Sincronize o projeto com os arquivos Gradle.

5. Execute o aplicativo em um emulador ou dispositivo físico.

### Aplicação Web

1. Navegue até o diretório da aplicação web:
   ```bash
   cd web-admin
   ```

2. Instale as dependências:
   ```bash
   npm install
   ```

3. Configure as variáveis de ambiente criando um arquivo `.env` na raiz do diretório `web-admin/`:
   ```env
   PORT=3000
   MONGODB_URI=mongodb://localhost:27017/flashbuy
   JWT_SECRET=seu_segredo_jwt
   API_URL=http://localhost:3000/api
   NODE_ENV=development
   ```

4. Inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   ```

5. Acesse a aplicação web em `http://localhost:3000`.

## Publicação do Aplicativo Android na Google Play Store

### Preparação do APK/AAB

1. No Android Studio, selecione `Build > Generate Signed Bundle/APK`.

2. Escolha entre Android App Bundle (AAB) ou APK. Recomendamos AAB para publicação na Play Store.

3. Crie ou selecione uma keystore existente:
   - Se for criar uma nova, preencha os campos necessários e guarde as informações em local seguro.
   - Se já tiver uma, selecione-a e forneça a senha.

4. Selecione o tipo de build `release` e clique em `Finish`.

5. O arquivo AAB/APK será gerado em `app/release/`.

### Publicação na Google Play Store

1. Acesse o [Google Play Console](https://play.google.com/console/).

2. Crie uma nova conta de desenvolvedor, se ainda não tiver uma (taxa única de $25 USD).

3. Clique em `Criar aplicativo` e preencha as informações básicas:
   - Nome do aplicativo
   - Idioma padrão
   - Tipo de aplicativo (Aplicativo ou Jogo)
   - Gratuito ou Pago

4. Complete todas as seções obrigatórias:
   - **Ficha da Play Store**: Descrições, capturas de tela, ícones, vídeos promocionais, etc.
   - **Classificação de conteúdo**: Preencha o questionário de classificação.
   - **Preço e distribuição**: Defina países de distribuição e preço (se aplicável).
   - **Configuração do aplicativo**: Privacidade, anúncios, classificação etária, etc.

5. Na seção `Produção`, clique em `Criar nova versão` e faça o upload do arquivo AAB/APK gerado anteriormente.

6. Adicione notas da versão e clique em `Salvar`.

7. Revise todas as informações e clique em `Iniciar lançamento para produção`.

8. Aguarde a revisão do Google, que pode levar de algumas horas a alguns dias.

### Dicas para Aprovação Rápida

- Certifique-se de que seu aplicativo segue as [Políticas do Desenvolvedor](https://play.google.com/about/developer-content-policy/).
- Forneça informações claras e precisas sobre o aplicativo.
- Inclua capturas de tela de alta qualidade que mostrem as principais funcionalidades.
- Teste minuciosamente o aplicativo antes de enviar para evitar crashes e bugs.
- Implemente uma política de privacidade adequada.
- Responda rapidamente a quaisquer solicitações do Google durante a revisão.

## Integração entre Aplicativo Android e Aplicação Web

A integração entre o aplicativo Android e a aplicação web é feita através de uma API RESTful. O aplicativo Android consome os endpoints da API para realizar operações como autenticação, gerenciamento de produtos, pedidos, etc.

A aplicação web administrativa fornece uma interface para gerenciar todos os aspectos do e-commerce, incluindo:

- Gerenciamento de usuários
- Gerenciamento de produtos e categorias
- Processamento de pedidos
- Análise de vendas e relatórios
- Configurações do sistema

A API está documentada usando Swagger e pode ser acessada em `http://localhost:3000/api-docs` quando o servidor estiver em execução.

## Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo LICENSE para detalhes.#   f l a s h b u y - e c o m m e r c e 
 
 