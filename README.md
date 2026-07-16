# Acertis — Site

Site estático (HTML puro, sem build, sem dependências além das fontes do Google).

## Estrutura

```
index.html          → site principal da Acertis (soluções, segmentos, Labs)
acertis-csm.html     → página dedicada do produto Acertis CSM
```

## Publicar no GitHub

```bash
cd acertis-site
git init
git add .
git commit -m "Site inicial da Acertis"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/acertis-site.git
git push -u origin main
```

(Crie o repositório vazio antes em github.com/new — sem README/gitignore, para não dar conflito no primeiro push.)

## Publicar no Vercel

1. Acesse vercel.com → **Add New... → Project**.
2. Importe o repositório `acertis-site` que você acabou de criar no GitHub.
3. Em **Framework Preset**, selecione **Other** (site estático, sem build).
4. Deixe **Build Command** e **Output Directory** em branco — o Vercel serve os arquivos da raiz automaticamente.
5. Clique em **Deploy**.

Depois do primeiro deploy, qualquer `git push` na branch `main` atualiza o site automaticamente.

## Domínio próprio (opcional)

Em **Project → Settings → Domains**, adicione seu domínio (ex: `acertis.com.br`) e siga as instruções de DNS que o Vercel mostrar (geralmente um registro `CNAME` ou `A`).
