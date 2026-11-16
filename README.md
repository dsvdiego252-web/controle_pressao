# Minha Pressão

Painel pessoal para registrar e consultar medições de pressão arterial (sistólica, diastólica, pulso, dose de enalapril e observações).

## Estrutura

```
index.html            Página principal
css/style.css         Estilos
js/app.js             Lógica (registro, gráfico, histórico, backup)
manifest.webmanifest  Permite "Adicionar à tela inicial" no celular
icon.svg              Ícone
vercel.json           Configuração de publicação na Vercel
```

Site estático, sem build e sem dependências.

## Como usar

- **Adicionar medição:** preencha o formulário e toque em *Salvar medição*. Opcionalmente informe uma 2ª leitura — o painel registra a média.
- **Consultar:** gráfico (7 dias, 30 dias, tudo), médias por dose e histórico com edição/exclusão.
- **Exportar:** *Exportar CSV* (abre no Excel) e *Imprimir* (para levar à consulta).

## Onde ficam os dados

Os registros ficam salvos **no navegador do aparelho** (localStorage). Não há servidor nem conta.
Por isso:

- Use **Backup JSON** com frequência.
- Para usar em outro aparelho, faça o backup em um e use **Importar JSON** no outro.
- Limpar os dados do navegador apaga os registros.

## Rodar localmente

Abra `index.html` no navegador, ou:

```bash
python3 -m http.server 8000
```

## Publicação

Publicado na Vercel como site estático (sem comando de build, diretório de saída = raiz).

> Este painel é apenas para acompanhamento e não substitui avaliação médica.
