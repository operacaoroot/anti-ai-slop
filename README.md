# anti-ai-slop

Skill do Claude Code que revisa texto em português antes da entrega. Ela lista as construções que denunciam texto gerado por IA ("não é X, é Y", "e isso muda tudo", "menos X, mais Y"), os títulos e aberturas de redação escolar, o dado citado sem fonte e o jargão de palco. No fim, roda um checklist de 8 itens em cada bloco do texto.

O Claude aciona a skill sozinho quando escreve ou revisa texto em PT-BR que vai para um público real. Também dá para chamar pelo nome: `/anti-ai-slop`.

## Instalação

Dentro do Claude Code:

```
/plugin marketplace add operacaoroot/anti-ai-slop
/plugin install anti-ai-slop@anti-ai-slop-marketplace
```

Sem o sistema de plugins, a alternativa é copiar o arquivo direto:

```bash
mkdir -p ~/.claude/skills/anti-ai-slop
cp plugins/anti-ai-slop/skills/anti-ai-slop/SKILL.md ~/.claude/skills/anti-ai-slop/
```

## Onde mexer

O conteúdo inteiro está em `plugins/anti-ai-slop/skills/anti-ai-slop/SKILL.md`. Ao mudar uma regra, suba a `version` em `plugins/anti-ai-slop/.claude-plugin/plugin.json` para que o `/plugin update` traga a versão nova.
