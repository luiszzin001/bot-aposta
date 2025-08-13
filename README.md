# Bot de Apostas Rematch (Discord)

Este bot foi desenvolvido para gerenciar apostas de partidas Rematch no Discord, com sistema de filas, pagamentos, pontuação e administração automatizada.

## Funcionalidades Principais
- **Filas Dinâmicas:** Criação e gerenciamento de filas para diferentes plataformas, modos e valores de aposta.
- **Pagamentos Automatizados:** Criação de canais de pagamento, exibição de PIX do admin responsável, fluxo de aprovação e fechamento automático.
- **Pontuação e Ranking:** Pontuação automática para vencedores, ranking de vitórias e consumo de pontos para apostar grátis.
- **Administração Simples:** Comandos para configurar admins, PIX, canais e permissões.
- **Limpeza de Mensagens:** Comando para limpar todas as mensagens de um canal rapidamente.

## Comandos Disponíveis

### Apostas e Filas
- `/fila` — Entrar em uma fila de aposta, escolhendo plataforma, modo e valor.
- `/definirganhador` — Admin define o vencedor, valor apostado e o bot calcula prêmio e pontos.
- `/ganhador` — (Alternativo) Admin define vencedor e prêmio manualmente.
- `/payapsaldo` — Jogador usa pontos acumulados para pagar uma aposta sem custo.
- `/ranking` — Exibe o ranking de vitórias dos jogadores.

### Administração
- `/setadmin` — Cadastrar admins responsáveis por apostas.
- `/configpixadm` — Configurar PIX do admin (banco, tipo, chave, titular).
- `/configcanais` — Configurar categoria/canais de pagamento.
- `/permadd`, `/permremove`, `/permlist` — Gerenciar permissões especiais de usuários.

### Utilidades
- `/clearmsg` — Limpa o máximo de mensagens possível do canal atual.
- `/say` — Envia mensagem personalizada pelo bot.

## Pontuação
- **Até 5,90:** 1 ponto por vitória
- **Acima de 5,90 até 20,90:** 2 pontos
- **Acima de 20,90 até 100,90:** 5 pontos
- Pontos podem ser usados para pagar apostas via `/payapsaldo` (consumo variável por valor)

## Instalação
1. **Clone o repositório:**
   ```bash
   git clone <repo-url>
   ```
2. **Instale as dependências:**
   ```bash
   npm install
   ```
3. **Configure o bot:**
   - Crie um bot no Discord Developer Portal e obtenha o token.
   - Configure variáveis de ambiente ou edite o arquivo de configuração, se necessário.
4. **Inicie o bot:**
   ```bash
   node index.js
   ```

## Estrutura dos Arquivos
- `Comandos/Cmds/` — Todos os comandos do bot (slash commands)
- `Database/` — Arquivos JSON para persistência de filas, admins, PIX, scores, etc.
- `Eventos/` — Eventos do Discord.js (ex: ready, message, interaction)
- `index.js` — Arquivo principal do bot

## Observações
- O bot só apaga mensagens de até 14 dias (limite Discord).
- Botões expiram após reiniciar o bot (limitação Discord).
- Todos os comandos estão documentados no código para fácil manutenção.

## Créditos
Desenvolvido por **Luis Devwzzl**

Se precisar de suporte, melhorias ou quiser contribuir, entre em contato!
