A proposta é criar formulários Web pelo HTML e após o preenchimento com os dados dos usuários, coletar e verificar os dados utilizando PHP.
O passo a passo do processo:
Passo 1:Criar o Formulário HTML
Crie um arquivo HTML chamado formulario.html com o seguinte conteúdo
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Passo 2: Criar o Arquivo PHP para Processar os Dados
Crie um arquivo PHP chamado "processar_formulario.ph" com o conteúdo doa rquivo anexado.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Passo 3: Configurar o Servidor para Enviar E-mails
Para que a função mail() do PHP funcione corretamente, o servidor web deve estar configurado para enviar e-mails. No caso de usar o XAMPP, MAMP ou WAMP, verifique a configuração do sendmail ou instale um servidor SMTP.

Passo 3.1:Verificando e Configurando sendmail no XAMPP (Windows)
Localize o arquivo php.ini:

Passo 3.2: Encontre o diretório onde o XAMPP está instalado (geralmente em C:\xampp).
Navegue até C:\xampp\php e abra o arquivo php.ini com um editor de texto.
Configuração do sendmail no php.ini:

Passo 3.3:Localize a seção [mail function] no arquivo php.ini.

Verifique se as linhas estão configuradas corretamente:

[mail function]
; For Win32 only.
; http://php.net/smtp
SMTP = smtp.seuprovedor.com
smtp_port = 25
; For Win32 only.
; http://php.net/sendmail-from
sendmail_from = seu-email@seuprovedor.com

Passo 3.4: Configuração do sendmail:
Navegue até C:\xampp\sendmail e abra o arquivo sendmail.ini com um editor de texto.

Passo 3.5:Configure os parâmetros no arquivo sendmail.ini:
[sendmail]

smtp_server=smtp.seuprovedor.com
smtp_port=587
auth_username=seu-email@seuprovedor.com
auth_password=sua-senha

; Or use your Gmail credentials
; smtp_server=smtp.gmail.com
; smtp_port=587
; auth_username=your-email@gmail.com
; auth_password=your-password

Passo 3.6:Reinicie o servidor XAMPP:
Depois de salvar as alterações, reinicie o servidor Apache através do painel de controle do XAMPP.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Passo 4: Testar a Aplicação
Coloque os arquivos formulario.html e processar_formulario.php no diretório do seu servidor web.
Acesse o formulário através do navegador, por exemplo, http://localhost/formulario.html.

Passo 5:Preencha o formulário e envie.
Verifique o e-mail seue-mailpessoal@algumeio.com para confirmar o recebimento dos dados.

Considerações Finais
Validação: Para produção, considere adicionar mais validações para os dados do formulário e proteger contra ataques de injeção.
Segurança: Use HTTPS para enviar dados sensíveis.
SMTP: Para uma solução de e-mail mais robusta, configure um servidor SMTP ou use uma biblioteca como PHPMailer.
