# ✦ Viral Studio — Cavaglieri

SaaS premium para criação de anúncios virais verticais 9:16 com IA generativa (Veo3 + Gemini).

## Stack

- **Frontend**: React 19 + TypeScript + Vite + Tailwind CSS v4
- **Animações**: Motion (Framer Motion)
- **IA Vídeo**: Google Veo3 via Vertex AI
- **IA Texto**: Gemini 2.5 Flash
- **Deploy**: Vercel (serverless functions)

## Setup Local

### 1. Instalar dependências
```bash
npm install
```

### 2. Configurar variáveis de ambiente
```bash
cp .env.example .env.local
```
Preencha o `.env.local` com suas chaves.

### 3. Rodar em desenvolvimento
```bash
npm run dev
```
Acesse: http://localhost:5173

## Deploy no Vercel

### 1. Conectar repositório
- Acesse [vercel.com](https://vercel.com)
- Importe o repositório `viral-studio-cavaglieri`

### 2. Configurar Environment Variables no painel do Vercel:
```
GEMINI_API_KEY=
GOOGLE_CLOUD_PROJECT_ID=viraliavideoscavaglieri
GOOGLE_CLOUD_LOCATION=us-central1
VEO_MODEL_ID=veo-3.0-generate-preview
GOOGLE_PRIVATE_KEY_ID=
GOOGLE_PRIVATE_KEY=
GOOGLE_CLIENT_EMAIL=
GOOGLE_CLIENT_ID=
GOOGLE_OAUTH_CLIENT_ID=
GOOGLE_OAUTH_CLIENT_SECRET=
APP_URL=https://seu-projeto.vercel.app
```

### 3. Deploy automático
Cada `git push` faz deploy automaticamente.

## APIs disponíveis

| Endpoint | Método | Descrição |
|----------|--------|-----------|
| `/api/health` | GET | Status da API |
| `/api/auth/url` | GET | URL OAuth Google Drive |
| `/api/drive/save` | POST | Salvar vídeo no Drive |
| `/api/veo/generate` | POST | Iniciar geração de vídeo |
| `/api/veo/status` | GET | Verificar status da geração |

## Segurança

⚠️ **NUNCA commite** os arquivos `.env`, `.env.local` ou arquivos JSON de credenciais Google.

---

Uso exclusivo da Sra. Mirian Soares Lima Cavaglieri.
