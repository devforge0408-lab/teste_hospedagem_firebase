# ⚒️ DevForge — Landing Page

Landing page do canal **DevForge** (programação e criação de sites), servida por um servidor **Node.js puro** — sem dependências externas.

A própria página ensina, passo a passo, como hospedar um site no **Firebase App Hosting** via integração com o GitHub.

## 🚀 Como rodar localmente

Pré-requisito: [Node.js](https://nodejs.org/) 18+

```bash
npm start
```

Acesse **http://localhost:3000**

## 📁 Estrutura do projeto

```
devforge-landing/
├── server.js        # Servidor HTTP em Node puro
├── package.json     # Script "start" para o App Hosting
└── public/
    ├── index.html   # Landing page (conteúdo do tutorial)
    └── style.css    # Estilos (tema dark "forja")
```

## ☁️ Deploy no Firebase App Hosting

O deploy é feito direto pelo **Firebase Console + GitHub**, sem CLI:

1. Faça push deste repositório para o GitHub.
2. No [Firebase Console](https://console.firebase.google.com/), crie um projeto (plano **Blaze**).
3. Vá em **Hosting & Serverless → App Hosting → Get started**.
4. Conecte sua conta do GitHub e selecione este repositório.
5. Configure: região, diretório raiz (`/`), live branch (`main`) e rollouts automáticos.
6. Clique em **Finish and deploy** — seu site vai para o ar em `*.hosted.app` com HTTPS.

A cada `git push` no live branch, um novo deploy acontece automaticamente (Cloud Build → Cloud Run → Cloud CDN).

> ⚠️ Importante: o `package.json` precisa do script `"start"` e o servidor deve escutar em `process.env.PORT` — ambos já configurados aqui.

## 📺 Sobre o canal

O **DevForge** ensina programação e criação de sites na prática: cada tutorial termina com um projeto real no ar. Inscreva-se e ative o sino!
