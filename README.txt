
🚚 TruckAdvisor Portugal - GUIA PASSO A PASSO (completo)

====================================
1. CRIAR CONTA NO CONTENTFUL
====================================
Acede a https://www.contentful.com, cria conta e entra.

1.1. Cria um novo espaço (space) chamado:
     ➤ TruckAdvisor Portugal

1.2. Vai a: Content Model > Add Content Type
     ➤ Nome: equipamento

1.3. Adiciona estes campos:
     - titulo (Short text)
     - marca (Short text)
     - modelo (Short text)
     - tipo (Short text)
     - preco (Number)
     - ano (Integer)
     - quilometragem (Integer)
     - normaEuro (Short text)
     - eixos (Integer)
     - descricao (Long text)
     - imagens (Media, multiple)
     - slug (Short text)

1.4. Vai a: Settings > API Keys > Add API Key
     ➤ Guarda:
        - Space ID
        - Content Delivery API - access token

====================================
2. USAR O CÓDIGO DO SITE
====================================

2.1. Instala o Node.js se ainda não tiveres: https://nodejs.org

2.2. Abre a pasta do projeto e cria o ficheiro `.env.local` com:
     NEXT_PUBLIC_CONTENTFUL_SPACE_ID=teu_space_id
     NEXT_PUBLIC_CONTENTFUL_ACCESS_TOKEN=teu_token

2.3. No terminal escreve:
     ➤ npm install
     ➤ npm run dev

2.4. O site ficará visível em:
     ➤ http://localhost:3000

====================================
3. PUBLICAR COM NETLIFY
====================================

3.1. Cria conta em https://netlify.com
3.2. Cria um novo site e liga ao teu repositório GitHub
3.3. Em “Site Settings > Environment Variables”, adiciona:
     ➤ NEXT_PUBLIC_CONTENTFUL_SPACE_ID = [teu ID]
     ➤ NEXT_PUBLIC_CONTENTFUL_ACCESS_TOKEN = [teu token]

3.4. Define “build command”:
     ➤ npm run build

3.5. Define “publish directory”:
     ➤ out

3.6. Associa o teu domínio personalizado (truckadvisorportugal.com)
3.7. Ativa HTTPS grátis (Let’s Encrypt)

Fim! Site online e ligado ao Contentful.

====================================
4. GESTÃO DO SITE
====================================

➤ Para adicionar/editar anúncios:
   Vais ao Contentful > Entries > Add Entry (tipo equipamento)
   Preenche os campos e publica

O site atualiza automaticamente após cada publicação ✅

