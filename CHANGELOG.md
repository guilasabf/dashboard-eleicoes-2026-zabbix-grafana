# Changelog

Formato inspirado em [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/). As datas são as da edição.

## TBD · próxima eleição

Itens identificados em 2026 e deixados para a próxima edição. Nenhum deles está em andamento.

- **Deputado Federal, Deputado Estadual e Deputado Distrital.** Cargos proporcionais, com mais de 18 mil candidatos no
  total (cerca de 7,3 mil, 10,7 mil e 415) e resultado por partido e federação. Pede uma visão própria no painel
  (placar por agremiação, eleitos e busca) em vez do formato de duelo usado em Presidente, Governador e Senador.
- **Resultados por município**, com mapa municipal e as capitais em destaque.
- **Eleições municipais (2028):** Prefeito e Vereador.
- **Endereço próprio e túnel nomeado**, para um link que não muda entre reinícios.
- **Versão enxuta na galeria de dashboards do Grafana**, nos moldes do painel de 2022.
- **Avaliar o plano gratuito do Grafana Cloud** (versão gerenciada) para hospedar o painel público na próxima
  eleição, no lugar do notebook, ou como reserva. Pontos a verificar: limites do plano, acesso público sem login e
  como conectar à coleta sem expor o Zabbix à internet.
- **Pessoa da comunidade para tocar a próxima edição**, com o apoio de quem já fez esta.

## 2026 · edição das Eleições Gerais

Agradecimento ao idealizador, Sansão Simonton (Telegram: @sansaoipb). Em memória de Magno Montecerqueira.

### Adicionado
- Apuração em tempo real de Presidente, Governador e Senador, para o Brasil, as 27 UFs e o exterior, com dados
  oficiais do TSE atualizados a cada 30 segundos.
- Descoberta automática de 833 candidatos, com foto oficial, vice, partido e coligação.
- Painel de duelo "Player 1 x Player 2", definido apenas pelos votos, e tela de pré-apuração com todos os candidatos
  em ordem de número.
- Mosaico do Brasil pelo líder de cada estado, tabelas por UF e página de detalhe de cada candidato.
- Medição de audiência com privacidade (versão restrita e versão agregada, sem IP).
- Página "Sobre", com contatos e apoio por Pix.
- Cinco máquinas virtuais em zonas separadas, exposição por túnel sem portas abertas e verificação ponta a ponta em um
  comando.
- Backup do banco de hora em hora e restauração ensaiada.

### Segurança e desempenho
- Painel público somente leitura, sem login e sem edição; 41 tentativas de invasão e edição testadas e recusadas.
- Capacidade medida de 260 para cerca de 1.300 espectadores simultâneos após três otimizações.
- Atualização fixa de 1 minuto no painel público.

### Aprendizados
- O túnel gratuito cai quando o notebook suspende; um vigia o religa, mas o endereço muda.
- Snapshot de máquina virtual ligada não é viável nessa configuração; o plano de recuperação usa backup de banco e
  snapshot de disco.
- Os arquivos do TSE também trazem eleições suplementares do ciclo; o código da eleição certa precisa ser escolhido com
  cuidado.
