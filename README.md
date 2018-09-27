# Buffalo
Repository for step-by-step on how to format a problematic buffalo nas

<b>** Não me responsabilizo pelo o que possa acontecer se você seguir este passo a passo **</b>

Necessário para o procedimento
- Firmware atualizada do NAS Buffalo
- TFTP com os arquivos de imagem do NAS Buffalo utilizado (pasta 
- NAS Navigator



1º Faça o clone deste repositório
2º Desligue o NAS
3º Altere o IP do computador para 192.168.11.1/24, ligue o NAS diretamente na porta lan do computador
4º Entre na pasta TFPT
5º Execute o arquivo TFTP Boot.exe
6º Ligue o NAS
7º Quando ele começar a piscar o led vermelho segure o botão função por 5 segundos, o led azul começará a piscar
8º Quando no TFTP aparecer duas linhas com a descrição "Block Served" o NAS comecará a piscar um led laranja (codigo 25), ele estará atualizando a firmware
9º Quando o led piscar azul,  acesse a pasta do firmware
10º Altere o arquivo LSUpdater.ini
11º Altere os dois campos da seção Flags
[Flags]
VersionCheck = 1 => 0
NoFormatting = 1 => 0
12º Adicione uma nova seção como abaixo
[SpecialFlags]
Debug = 1
13º Execute o programa LSUpdater.exe
14º Clique em Update, ele irá pedir para formatar, aceite, começará a passar o novo firmware, o processo é um pouco demorado
15º Após o processo o NAS será acessivel pelo NAS NAVIGADOR
16º Inicialmente a interface web estará em japonês, para corrigir acesse com admin(usuário) e password(senha)
17º No menu a quarta opção(fica abaixo do 'O' de buffalo)
18º No terceiro menu de dropdown estará o campo da linguagem, clique no botão a esquerda.
19º


Links que podem ajudar: (acessiveis em 27/09/2018)
https://www.reddit.com/r/sysadmin/comments/74xoju/how_to_fix_a_buffalo_terastation_tsxel_in_tftp/ 
http://forums.buffalotech.com/index.php?topic=10185.0
https://fatmin.com/2015/02/08/how-to-fix-the-buffalo-linkstation-nas-partition-not-found-error/
http://www.herzig-net.de/prog/?page=unbrick_ls-wxl
