# Fichário Riftbound — versão 1

Site estático HTML/CSS/JS para Vercel. Duas cartas reais no JSON são **exemplos para demonstração**, não estoque real. Substitua pelo seu inventário antes de divulgar o link.

## Testar no computador
Abra esta pasta no VS Code e use Live Server; ou abra um terminal e rode:

```bash
python -m http.server 8000
```

Acesse http://localhost:8000 (abrir index.html diretamente pelo arquivo não funciona com fetch de JSON).

## Configurar WhatsApp
Abra `script.js`, substitua `5555999999999` em `WHATSAPP_NUMERO` pelo seu telefone no formato 55 + DDD + número, sem `+`, espaços ou traços.

## Cadastrar novas cartas
Edite `cartas.json`: uma entrada por carta/variante, incluindo foil separado de normal. Identificadores (`id`) devem ser únicos e estáveis. `estoque` é número inteiro. `imagem` pode ser URL HTTPS do catálogo autorizado ou caminho local `imagens/nome.png`. Não use os dados de exemplo como se fossem estoque real.

## Publicar na Vercel
Crie repositório no GitHub com estes arquivos na raiz, em Vercel: Add New > Project > Import repository. Framework Preset: Other; Build Command: vazio; Output Directory: vazio (raiz). Publique o projeto. Atualizações em `cartas.json` enviadas ao GitHub disparam novo deploy automático, com integração Git habilitada.

## Limites desta versão
Nenhuma reserva nem baixa automática de estoque ocorre quando se clica no WhatsApp. O site não tem painel de administrador nem persistência remota; alterações de estoque precisam ser publicadas. Scanner em `scanner/` será construído na fase 2. Imagens externas podem ter restrições de uso ou expirar: confirme direitos e prefira assets autorizados.
