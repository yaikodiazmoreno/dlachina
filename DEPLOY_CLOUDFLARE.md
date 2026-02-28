# Publicar en Cloudflare Pages (usando GitHub)

## 1) Inicializar Git y subir a GitHub
En tu terminal, dentro de esta carpeta, ejecuta:

```bash
git init
git add .
git commit -m "feat: sitio estático inicial"

git branch -M main
git remote add origin https://github.com/TU_USUARIO/TU_REPO.git
git push -u origin main
```

> Reemplaza `TU_USUARIO` y `TU_REPO` con tu repositorio real.

## 2) Crear proyecto en Cloudflare Pages
1. Entra a Cloudflare Dashboard.
2. Ve a **Workers & Pages** → **Create application** → **Pages**.
3. Selecciona **Connect to Git** y autoriza GitHub.
4. Elige tu repositorio.

## 3) Configuración de build (sitio estático puro)
- **Framework preset:** None
- **Build command:** (vacío)
- **Build output directory:** `.`
- **Root directory:** (vacío)

Después, presiona **Save and Deploy**.

## 4) Dominio personalizado (opcional)
1. En tu proyecto Pages: **Custom domains** → **Set up a custom domain**.
2. Escribe tu dominio y sigue el asistente DNS.

## 5) Publicaciones futuras
Cada `git push` a `main` dispara un deploy automático.

```bash
git add .
git commit -m "chore: cambios"
git push
```
