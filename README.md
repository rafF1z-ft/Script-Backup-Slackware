# Script de Backup para Slackware

Este é um script em Shell Script desenvolvido para realizar backups periódicos em um HD externo.

Como usuário do Slackware, costumo formatar o sistema a cada 6 meses, seguido pela mesma pós-instalação, que inclui o download manual dos mesmos arquivos.

Desenvolvi este script simples para efetuar um backup completo de um diretório específico, simplificando assim todo o processo. Tenho outros scripts de automação escritos em Shell, os quais pretendo compartilhar posteriormente. Embora não seja meu hábito comentar códigos, este script está bem documentado para facilitar o entendimento, sendo projetado para meu uso pessoal.

**Modo de Uso:**
1. Baixe o arquivo e conceda permissão de execução (`chmod +x bkp-completo.sh`).
2. Mova o arquivo para: `mv /usr/local/sbin/bkp-completo.sh`.
3. (Opcional) Crie uma abreviação no arquivo `.bashrc` com o seguinte comando: `alias log-bkp="cat /var/log/daily-backup.log"` para visualizar o log do backup com apenas o comando `log-bkp`.
4. Execute o script via terminal com `bkp-completo.sh`.
5. Verifique o log (`/var/log/daily-backup.log`) para saber se a operação foi bem-sucedida, pois o resultado não é exibido na tela. Dependendo do tamanho, a execução pode demorar alguns minutos.

Esteja atento ao arquivo de log para obter detalhes importantes sobre o processo de backup, incluindo possíveis erros ou mensagens informativas.

Ele também possui a funcionalidade de remover automaticamente arquivos que têm mais de 90 dias (esse valor é ajustável de acordo com a preferência do usuário).
