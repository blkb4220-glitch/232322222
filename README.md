# 🎬 Portfólio Murilo - Editor de Vídeo

Portfólio profissional otimizado para editor de vídeo especializado em After Effects, motion graphics e conteúdo viral.

## ✨ Melhorias Implementadas

### SEO & Performance
- ✅ Meta tags completas (description, keywords, Open Graph, Twitter Cards)
- ✅ Favicon personalizado
- ✅ robots.txt configurado
- ✅ Lazy loading em imagens
- ✅ Smooth scroll
- ✅ Otimização de acessibilidade (ARIA labels)

### Design & UX
- ✅ Menu mobile responsivo com animação hamburger
- ✅ Seção de portfólio com grid de projetos
- ✅ Modal para visualizar detalhes dos projetos
- ✅ Botões de CTA otimizados
- ✅ Animações profissionais suaves
- ✅ Navegação melhorada

### Funcionalidades
- ✅ Contador de visitantes (requer backend)
- ✅ Links sociais (Discord, TikTok)
- ✅ Navegação por âncoras
- ✅ Responsividade completa

## 🚀 Deploy

### Opção 1: Render (Recomendado)

O Render suporta o servidor Node.js e banco de dados SQLite.

1. Crie um novo **Web Service** no [Render](https://render.com)
2. Conecte ao seu repositório GitHub
3. Configure as **Environment Variables**:
   - `NIXPACKS_PKGMGR` = `pnpm`
4. Configure em **Settings**:
   - **Build Command**: `pnpm install && pnpm build`
   - **Start Command**: `pnpm start`
5. Configure **Persistent Disk** em **Disks**:
   - **Name**: `sqlite-data`
   - **Mount Path**: `/opt/render/project/src/dist`

### Opção 2: Railway

1. Crie um novo projeto no [Railway](https://railway.app)
2. Conecte ao seu repositório
3. Configure em **Settings**:
   - **Build Command**: `pnpm install && pnpm build`
   - **Start Command**: `pnpm start`
4. Configure **Volume** em **Volumes**:
   - **Path**: `/app/dist`

### Opção 3: Netlify (Apenas Frontend - Sem contador)

1. Conecte ao [Netlify](https://netlify.com)
2. Configure:
   - **Build Command**: `pnpm install && pnpm run build`
   - **Publish Directory**: `dist/public`

⚠️ **Nota**: No Netlify o contador de visitantes não funcionará pois não há backend.

## 🛠️ Desenvolvimento Local

```bash
# Instalar dependências
pnpm install

# Rodar em desenvolvimento
pnpm dev

# Build para produção
pnpm build

# Preview da build
pnpm preview
```

## 📁 Estrutura do Projeto

```
portfolio-otimizado/
├── client/
│   ├── public/
│   │   ├── assets/          # Imagens e recursos
│   │   ├── favicon.svg      # Favicon personalizado
│   │   └── robots.txt       # SEO
│   ├── src/
│   │   ├── components/
│   │   │   ├── ui/          # Componentes UI base
│   │   │   ├── MobileMenu.tsx
│   │   │   ├── PortfolioSection.tsx
│   │   │   └── TypingEffect.tsx
│   │   ├── pages/
│   │   │   └── Home.tsx     # Página principal
│   │   ├── lib/
│   │   │   └── data.ts      # Dados de projetos e skills
│   │   └── index.css        # Estilos globais
│   └── index.html           # HTML com meta tags
├── server/                  # Backend Node.js
└── package.json
```

## 🎨 Personalização

### Adicionar Projetos

Edite `client/src/lib/data.ts`:

```typescript
export const projects: Project[] = [
  {
    id: 1,
    title: "Nome do Projeto",
    category: "Categoria",
    description: "Descrição do projeto...",
    thumbnail: "/assets/thumbnail.jpg",
    tags: ["Tag1", "Tag2", "Tag3"],
  },
  // ... mais projetos
];
```

### Alterar Cores

Edite as variáveis CSS em `client/src/index.css`:

```css
:root {
  --primary: oklch(0.62 0.28 35); /* Laranja vibrante */
  --accent: oklch(0.65 0.30 30);  /* Laranja claro */
  /* ... outras cores */
}
```

### Adicionar Imagens

1. Coloque as imagens em `client/public/assets/`
2. Use formato WebP para melhor performance
3. Referencie como `/assets/nome-da-imagem.webp`

## 📊 SEO

O site está otimizado para SEO com:
- Título descritivo
- Meta description
- Keywords relevantes
- Open Graph tags (Facebook)
- Twitter Cards
- Estrutura semântica HTML5
- Alt text em imagens

## 🔧 Tecnologias

- **Frontend**: React + TypeScript + Vite
- **Styling**: TailwindCSS
- **UI Components**: Shadcn/ui
- **Backend**: Node.js + Express
- **Database**: SQLite
- **Fonts**: Playfair Display + Manrope

## 📝 Licença

© 2024 murlxz.outt - Todos os direitos reservados.

---

**Desenvolvido com ❤️ para profissionais criativos**
