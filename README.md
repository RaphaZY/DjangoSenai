<h1 align="center">
  <br>
  <a href="#"><img src="https://github.com/IMNascimento/DVR/assets/28989407/84028706-5a9e-4d00-af2c-2935e5604035" alt="Nascimento" width="200"></a>
  <br>
  Nascimento
  <br>
</h1>

## Descrição:
<p>Nesse repositorio iremos realizar um passo a passo de criação de uma aplicação em django, para ficar de base para consulta dos alunos. Todos procedimentos de configurações será realizados e documentado para auxilio do desenvolvimento individual de cada um dos alunos no programa Trilhas de Futuro.</p>

# Passo a Passo

## Pré-requisitos:
-Instalação do Mysql: [Mysql](https://dev.mysql.com/downloads/installer/)<br>
-Instalação do Python: [Python](https://www.python.org/downloads/)<br>
-Instalação do Workbeanch: [WorkBeanch](https://dev.mysql.com/downloads/workbench/)<br>
-Instalação do VSCode: [VSCode](https://code.visualstudio.com/download)<br>

## 0- Criação de VENV e instalação do Django:
<b>0.0-</b> Código para criar a VENV "python -m venv 'nome_do_ambiente_virtual': "
```bash
python3 -m venv igor
```
<b>0.1-</b> Ativando a VENV windows "nome_da_venv\Scripts\activate":
```bash
 C:\python\Django> .\igor\Script\activate 
```
<b>0.2-</b> Verificando se a VENV está ativa pelo <b>VSCode</b>:<br>
    - Caso a sua Venv esteja ativa você vai verificar um nome dela na frete do caminho da pasta igual a imagem abaixo. 
    <br><br>
![venv](https://github.com/IMNascimento/DjangoSenai/assets/28989407/424b222b-40ea-48b6-8568-ff43cf9e99d7)
<br><br>
**0.3-** Instalando o Django:
```bash
 (igor)C:\python\Django> pip install django
```
**0.4-** Iniciando um projeto Django com o comando "django-admin startproject 'nome_do_projeto'":
```bash
 (igor)C:\python\Django> django-admin startproject trilhas
```
## 1- Servidor Django:
Após iniciar um projeto Django devemos inicializar um servidor para testarmos nossa aplicação, para isso iremos fazer os seguintes passos.<br><br>
**1.0-** Iniciar um servidor "python manage.py runserver":
```bash
(igor)C:\python\Django> cd trilhas
(igor)C:\python\Django\trilhas> python manage.py runserver
```
**1.1-** Verifique se o servidor funcionou normalmente acessando o endereço "127.0.0.1:8000":<br>
    - Caso tenha funcionado corretamente ele irá aparecer a imagem abaixo.<br><br>
![dajngo](https://github.com/IMNascimento/DjangoSenai/assets/28989407/888d6c30-7939-4085-a02f-e6f6df3938a3)
<br>
    - Caso queira trocar de porta ou ip de acesso inicie com o código "python manage.py runserver 0.0.0.0:0000" no lugares do zero você vai passar o ip e a porta.<br>
    - Agora podemos criar varios aplicativos dentro do nosso projeto.<br><br>
**1.2-** Criando um aplicativo "python manage.py startapp nome_do_aplicativo":
```bash
(igor)C:\python\Django\trilhas> python manage.py startapp siteTrilhas
```
## 2- Registrando App no Django:
**2.0-** Para verificar o nome do app criado você vai na pasta do app no arquivo app.py, vamos demonstrar com a foto abaixo:<br>
![app](https://github.com/IMNascimento/DjangoSenai/assets/28989407/b64f64ae-4e7e-47b1-8316-73c4501809cb)<br>
-Como podemos verificar na foto temos em vermelho o sistema de diretorio até o arquivo e destacado de verde temos o nome do nosso app.<br>
**2.1-** Agora vamos registrar esse app vamos na pasta do nosso projeto e encontraremos o arquivo "settings.py" nele iremos inserir o nome da nossa aplicação como iremos verificar na foto a seguir:<br>
![registro](https://github.com/IMNascimento/DjangoSenai/assets/160553204/b3e260f9-1fbe-4ebf-81a3-8bd9f5780870)
<br>
-Deixamos novamente com a cor vermelho o sistema de diretorio até o arquivo e marcado de verde a linha com nome que seria inserido.<br>
- Agora que nossa aplicação já foi cadastrada podemos testar se ela irá funcionar corretamente. Para isso precisaremos criar urls para o carregamento externo de nossa página. Veremos essa criação na próxima etapa.

## 3- Criando Url no App Django:
**3.0-** Criação de um arquivo urls.py dentro do seu app que no nosso caso chama "siteTrilhas":<br>
![url](https://github.com/IMNascimento/DjangoSenai/assets/28989407/1b3bf2eb-b78c-4c4b-8693-254a718bdb19)<br>
**3.1-** Quando criarmos esse arquivo url o editor irá informa que não existe o método para isso iremos criar ele em seguida.<br>
![view](https://github.com/IMNascimento/DjangoSenai/assets/28989407/eb553e1c-4356-4980-800d-ad52bb5fd3d6)<br>
**3.2-** Como vimos na imagem acima criamos uma view para exibir um texto "Olá mundo." na nossa página web. Por último Precisamos registrar nossas rotas. <br>
![rotas](https://github.com/IMNascimento/DjangoSenai/assets/160553204/ab165b57-654b-4c14-968d-d939bbaf8d3c)<br>
- Agora registramos nossa rota basta apenas você acessar e verificar se o acesso funcionou corretamente na web. Deixamos marcado de vermelho na imagem o sistema de diretorio para o seu auxilio e deixamos na marcação verde os itens que deve ser adicionado no seu arquivo para o funcionamento correto.

## 4- Criando Templates no App Django:
**4.0-** Primeiro dentro da pasta do seu app crie uma pasta chamada templates. No nosso casso nosso app chama "siteTrilhas" e dentro dessa pasta nós iremos criar uma pasta chamada "templates".<br>
**4.1-** Dentro dessa pasta crie um arquivo chamado index.html e coloque os seguintes códigos: 
```html5
<!DOCTYPE html>
<html lang="pt-br">
<head>
<title>Teste Template</title>
</head>
<body>
<h1>Estamos criando um template.</h1>
</body>
</html>
```
**4.2-** Agora vá no arquivo de view.py e coloque o código como está a imagem abaixo:<br>
![viewtemplate](https://github.com/IMNascimento/DjangoSenai/assets/28989407/3bf38177-dc78-43a2-afe9-d296a009de0c)<br>
**4.3-** Agora vá ao arquivo de urls.py e coloque o código a baixo:<br>
![template](https://github.com/IMNascimento/DjangoSenai/assets/28989407/3782f1fd-f47d-4780-a344-2db876d54c58)<br>
-Pronto após execução desses passos tente acessar o endereço 127.0.0.1:8000/pagina o acesso tem que ocorrer corretamente.

## 5- Criando e carregando arquivos estáticos Django:
**5.0-** Vamos no arquivo settings.py na pasta do seu projeto e na linha de templates altere como vai demonstrar a foto a baixo:<br>
![os](https://github.com/IMNascimento/DjangoSenai/assets/28989407/69b21f1e-fe85-409b-ac94-f46aea5a3048)<br>
**5.1-** Esse import OS nós adicionamos no inicio do arquivo settings.py.<br>
![temp](https://github.com/IMNascimento/DjangoSenai/assets/28989407/cbbdea71-6f9d-47f5-997b-291613c8884d)<br>
**5.2-** Agora circulado de vermelho temos o codigo que devemos colocar. Além dessas alterações temos que colocar no final do nosso arquivo o files statics como veremos na foto a seguir.<br>
![static](https://github.com/IMNascimento/DjangoSenai/assets/28989407/2b6124f7-d661-4919-b8fc-0bb3dd18b806)<br>
**5.3-** Como vemos na imagem a cima passamos um caminho de uma pasta static dentro de "trilhas/static", essa pasta static vai precisar ser criada na pastat base do seu projeto.<br>
**5.4-** Agora nesse projeto peque as pastas css, js, imagens e todos os itens de estilos e de javascript que vocês tiverem e coloquem dentro dessa pasta static.<br>
**5.5-** Após colocar os arquivos você precisa executar o comando para o django visualizar os novos arquivos o comando é "python .\manage.py collectstatic" lembrando que para executar os comandos você tem que estar dentro da pasta do trilhas:<br>
```bash
C:\DjangoSenai\trilhas> python .\manage.py collectstatic
```
**5.6-** Agora vamos trocar o código do nosso index.html que está dentro da pasta template no nosso app:<br>
```html5
<!DOCTYPE HTML>
<html>
	<head>
		<title>Fractal by HTML5 UP</title>
		<meta charset="utf-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no" />
		<link rel="stylesheet" href="assets/css/main.css" />
		<noscript><link rel="stylesheet" href="assets/css/noscript.css" /></noscript>
	</head>
	<body class="is-preload">

		<!-- Header -->
			<header id="header">
				<div class="content">
					<h1><a href="#">Fractal</a></h1>
					<p>Just a simple, single page responsive<br />
					template brought to you by <a href="http://html5up.net">HTML5 UP</a></p>
					<ul class="actions">
						<li><a href="#" class="button primary icon solid fa-download">Download</a></li>
						<li><a href="#one" class="button icon solid fa-chevron-down scrolly">Learn More</a></li>
					</ul>
				</div>
				<div class="image phone"><div class="inner"><img src="images/screen.jpg" alt="" /></div></div>
			</header>

		<!-- One -->
			<section id="one" class="wrapper style2 special">
				<header class="major">
					<h2>Sed ipsum magna lorem tempus amet<br />
					vehicula et gravida elementum</h2>
				</header>
				<ul class="icons major">
					<li><span class="icon solid fa-camera-retro"><span class="label">Shoot</span></span></li>
					<li><span class="icon solid fa-sync"><span class="label">Process</span></span></li>
					<li><span class="icon solid fa-cloud"><span class="label">Upload</span></span></li>
				</ul>
			</section>

		<!-- Two -->
			<section id="two" class="wrapper">
				<div class="inner alt">
					<section class="spotlight">
						<div class="image"><img src="images/pic01.jpg" alt="" /></div>
						<div class="content">
							<h3>Magna sed ultrices</h3>
							<p>Morbi mattis ornare ornare. Duis quam turpis, gravida at leo elementum elit fusce accumsan dui libero, quis vehicula lectus ultricies eu. In convallis amet leo non sapien iaculis efficitur consequat lorem ipsum.</p>
						</div>
					</section>
					<section class="spotlight">
						<div class="image"><img src="images/pic02.jpg" alt="" /></div>
						<div class="content">
							<h3>Ultrices nullam aliquam</h3>
							<p>Morbi mattis ornare ornare. Duis quam turpis, gravida at leo elementum elit fusce accumsan dui libero, quis vehicula lectus ultricies eu. In convallis amet leo non sapien iaculis efficitur consequat lorem ipsum.</p>
						</div>
					</section>
					<section class="spotlight">
						<div class="image"><img src="images/pic03.jpg" alt="" /></div>
						<div class="content">
							<h3>Aliquam sed magna</h3>
							<p>Morbi mattis ornare ornare. Duis quam turpis, gravida at leo elementum elit fusce accumsan dui libero, quis vehicula lectus ultricies eu. In convallis amet leo non sapien iaculis efficitur consequat lorem ipsum.</p>
						</div>
					</section>
					<section class="special">
						<ul class="icons labeled">
							<li><span class="icon solid fa-camera-retro"><span class="label">Ipsum lorem accumsan</span></span></li>
							<li><span class="icon solid fa-sync"><span class="label">Sed vehicula elementum</span></span></li>
							<li><span class="icon solid fa-cloud"><span class="label">Elit fusce consequat</span></span></li>
							<li><span class="icon solid fa-code"><span class="label">Lorem nullam tempus</span></span></li>
							<li><span class="icon solid fa-desktop"><span class="label">Adipiscing amet sapien</span></span></li>
						</ul>
					</section>
				</div>
			</section>

		<!-- Three -->
			<section id="three" class="wrapper style2 special">
				<header class="major">
					<h2>Magna leo sapien gravida</h2>
					<p>Gravida at leo elementum elit fusce accumsan dui libero, quis vehicula<br />
					lectus ultricies eu. In convallis amet leo sapien iaculis efficitur.</p>
				</header>
				<ul class="actions special">
					<li><a href="#" class="button primary icon solid fa-download">Download</a></li>
					<li><a href="#" class="button">Learn More</a></li>
				</ul>
			</section>

		<!-- Footer -->
			<footer id="footer">
				<ul class="icons">
					<li><a href="#" class="icon brands fa-facebook-f"><span class="label">Facebook</span></a></li>
					<li><a href="#" class="icon brands fa-twitter"><span class="label">Twitter</span></a></li>
					<li><a href="#" class="icon brands fa-instagram"><span class="label">Instagram</span></a></li>
				</ul>
				<p class="copyright">&copy; Untitled. Credits: <a href="http://html5up.net">HTML5 UP</a></p>
			</footer>

		<!-- Scripts -->
			<script src="assets/js/jquery.min.js"></script>
			<script src="assets/js/jquery.scrolly.min.js"></script>
			<script src="assets/js/browser.min.js"></script>
			<script src="assets/js/breakpoints.min.js"></script>
			<script src="assets/js/util.js"></script>
			<script src="assets/js/main.js"></script>

	</body>
</html>
```

**5.7-** Antes de testar agora vamos alterar os códigos da nossa inde.html para que ele possa encherga agora nosso css, js. No inicio do arquivo vamos colocar o {% load static %} e em cada link vamos colocar {% static 'caminho_do_seu_item/' %} como veremos os códigos a seguir:<br>
```html5
{% load static %}
<!DOCTYPE HTML>
<html>
	<head>
		<title>Nascimento</title>
		<meta charset="utf-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no" />
		<link rel="stylesheet" href="{% static 'assets/css/main.css' %}" />
		<noscript><link rel="stylesheet" href="{% static 'assets/css/noscript.css' %}" /></noscript>
	</head>
	<body class="is-preload">

		<!-- Header -->
			<header id="header">
				<div class="content">
					<h1><a href="#">Igor Nascimento</a></h1>
					<p>Aqui você colocara um curriculo seu,<br />
					no formato de pdf para ser baixado</p>
					<ul class="actions">
						<li><a href="#" class="button primary icon solid fa-download">Download</a></li>
						<li><a href="#one" class="button icon solid fa-chevron-down scrolly">Learn More</a></li>
					</ul>
				</div>
				<div class="image phone"><div class="inner"><img src="{% static 'images/screen.jpg' %}" alt="" /></div></div>
			</header>

		<!-- One -->
			<section id="one" class="wrapper style2 special">
				<header class="major">
					<h2>Seus principais serviços<br />
					você colocara aqui</h2>
				</header>
				<ul class="icons major">
					<li><span class="icon solid fa-camera-retro"><span class="label">Shoot</span></span></li>
					<li><span class="icon solid fa-sync"><span class="label">Process</span></span></li>
					<li><span class="icon solid fa-cloud"><span class="label">Upload</span></span></li>
				</ul>
			</section>

		<!-- Two -->
			<section id="two" class="wrapper">
				<div class="inner alt">
					<section class="spotlight">
						<div class="image"><img src="{% static 'images/pic01.jpg' %}" alt="" /></div>
						<div class="content">
							<h3>Magna sed ultrices</h3>
							<p>Morbi mattis ornare ornare. Duis quam turpis, gravida at leo elementum elit fusce accumsan dui libero, quis vehicula lectus ultricies eu. In convallis amet leo non sapien iaculis efficitur consequat lorem ipsum.</p>
						</div>
					</section>
					<section class="spotlight">
						<div class="image"><img src="{% static 'images/pic02.jpg' %}" alt="" /></div>
						<div class="content">
							<h3>Ultrices nullam aliquam</h3>
							<p>Morbi mattis ornare ornare. Duis quam turpis, gravida at leo elementum elit fusce accumsan dui libero, quis vehicula lectus ultricies eu. In convallis amet leo non sapien iaculis efficitur consequat lorem ipsum.</p>
						</div>
					</section>
					<section class="spotlight">
						<div class="image"><img src="{% static 'images/pic03.jpg'%}" alt="" /></div>
						<div class="content">
							<h3>Aliquam sed magna</h3>
							<p>Morbi mattis ornare ornare. Duis quam turpis, gravida at leo elementum elit fusce accumsan dui libero, quis vehicula lectus ultricies eu. In convallis amet leo non sapien iaculis efficitur consequat lorem ipsum.</p>
						</div>
					</section>
					<section class="special">
						<ul class="icons labeled">
							<li><span class="icon solid fa-camera-retro"><span class="label">cada icone seus serviços</span></span></li>
							<li><span class="icon solid fa-sync"><span class="label">Sed vehicula elementum</span></span></li>
							<li><span class="icon solid fa-cloud"><span class="label">Elit fusce consequat</span></span></li>
							<li><span class="icon solid fa-code"><span class="label">Lorem nullam tempus</span></span></li>
							<li><span class="icon solid fa-desktop"><span class="label">Adipiscing amet sapien</span></span></li>
						</ul>
					</section>
				</div>
			</section>

		<!-- Three -->
			<section id="three" class="wrapper style2 special">
				<header class="major">
					<h2>Seu nome completo </h2>
					<p>Um pouco sobre você e depois insira novamente o pdf<br />
					com o seu curriculo para download.</p>
				</header>
				<ul class="actions special">
					<li><a href="#" class="button primary icon solid fa-download">Download</a></li>
					<li><a href="#" class="button">Learn More</a></li>
				</ul>
			</section>

		<!-- Footer -->
			<footer id="footer">
				<ul class="icons">
					<li><a href="#" class="icon brands fa-facebook-f"><span class="label">Facebook</span></a></li>
					<li><a href="#" class="icon brands fa-twitter"><span class="label">Twitter</span></a></li>
					<li><a href="#" class="icon brands fa-instagram"><span class="label">Instagram</span></a></li>
				</ul>
				<p class="copyright">&copy; Untitled. Credits: <a href="http://html5up.net">HTML5 UP</a> , <a href="#">Nascimento</a> </p>
			</footer>

		<!-- Scripts -->
			<script src="{% static 'assets/js/jquery.min.js' %}"></script>
			<script src="{% static 'assets/js/jquery.scrolly.min.js' %}"></script>
			<script src="{% static 'assets/js/browser.min.js' %}"></script>
			<script src="{% static 'assets/js/breakpoints.min.js' %}"></script>
			<script src="{% static 'assets/js/util.js' %}"></script>
			<script src="{% static 'assets/js/main.js' %}"></script>

	</body>
</html>
```
**5.8-** Após ter executado esses passos acesse o navegador no endereço 127.0.0.1:8000 e teste verifique se seu layout apareceu corretamente.<br>
## 6- Criando Layout com extends no Django:
**6.0-** O conceito DRY é muito ativo no Django e se você reparar todo inicio de código html é o mesmo em todas as páginas e isso é uma repetição desnecessaria. Para reutilização desses códigos usamos o extends. Vamos pegar todo nosso conteudo da primeira linha até a tag body e  quase no final da pagina vamos pegar também os códigos desde a tag script até o final, recorta para um arquivo que vamos fazer que é o layout.html.Vou deixar o código de como vai ficar esse novo arquivo layout.html:
```python

{% load static %}
<!DOCTYPE HTML>
<html>
	<head>
		<title>Nascimento</title>
		<meta charset="utf-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no" />
		<link rel="stylesheet" href="{% static 'assets/css/main.css' %}" />
		<noscript><link rel="stylesheet" href="{% static 'assets/css/noscript.css' %}" /></noscript>
	</head>
	<body class="is-preload">

    {% block content %} 
    {% endblock %}
    <!-- Scripts -->
        <script src="{% static 'assets/js/jquery.min.js' %}"></script>
        <script src="{% static 'assets/js/jquery.scrolly.min.js' %}"></script>
        <script src="{% static 'assets/js/browser.min.js' %}"></script>
        <script src="{% static 'assets/js/breakpoints.min.js' %}"></script>
        <script src="{% static 'assets/js/util.js' %}"></script>
        <script src="{% static 'assets/js/main.js' %}"></script>

	</body>
</html>
```
**6.1-** Como vimos a cima usamos o {% block content %} para informa que teremos um block de conteudo ali dentro e usamos o {% endblock %} para mostrar o final do conteudo inserido. Agora para poder funcionar o layout temos que fazer algumas alteração no nosso index.html como a utilização do  {% block content %} par informa o inicio do conteudo e o {% extends 'nome_do_arquivo' %} para informa de qual layout você está puxando essas informações. Vou deixar o código do index.html para vocês verificarem o uso desses itens:

```python
{% extends 'layout.html' %}
{% load static %}
{% block content %}
		<!-- Header -->
			<header id="header">
				<div class="content">
					<h1><a href="#">Igor Nascimento</a></h1>
					<p>Aqui você colocara um curriculo seu,<br />
					no formato de pdf para ser baixado</p>
					<ul class="actions">
						<li><a href="#" class="button primary icon solid fa-download">Download</a></li>
						<li><a href="#one" class="button icon solid fa-chevron-down scrolly">Learn More</a></li>
					</ul>
				</div>
				<div class="image phone"><div class="inner"><img src="{% static 'images/screen.jpg' %}" alt="" /></div></div>
			</header>

		<!-- One -->
			<section id="one" class="wrapper style2 special">
				<header class="major">
					<h2>Seus principais serviços<br />
					você colocara aqui</h2>
				</header>
				<ul class="icons major">
					<li><span class="icon solid fa-camera-retro"><span class="label">Shoot</span></span></li>
					<li><span class="icon solid fa-sync"><span class="label">Process</span></span></li>
					<li><span class="icon solid fa-cloud"><span class="label">Upload</span></span></li>
				</ul>
			</section>

		<!-- Two -->
			<section id="two" class="wrapper">
				<div class="inner alt">
					<section class="spotlight">
						<div class="image"><img src="{% static 'images/pic01.jpg' %}" alt="" /></div>
						<div class="content">
							<h3>Magna sed ultrices</h3>
							<p>Morbi mattis ornare ornare. Duis quam turpis, gravida at leo elementum elit fusce accumsan dui libero, quis vehicula lectus ultricies eu. In convallis amet leo non sapien iaculis efficitur consequat lorem ipsum.</p>
						</div>
					</section>
					<section class="spotlight">
						<div class="image"><img src="{% static 'images/pic02.jpg' %}" alt="" /></div>
						<div class="content">
							<h3>Ultrices nullam aliquam</h3>
							<p>Morbi mattis ornare ornare. Duis quam turpis, gravida at leo elementum elit fusce accumsan dui libero, quis vehicula lectus ultricies eu. In convallis amet leo non sapien iaculis efficitur consequat lorem ipsum.</p>
						</div>
					</section>
					<section class="spotlight">
						<div class="image"><img src="{% static 'images/pic03.jpg'%}" alt="" /></div>
						<div class="content">
							<h3>Aliquam sed magna</h3>
							<p>Morbi mattis ornare ornare. Duis quam turpis, gravida at leo elementum elit fusce accumsan dui libero, quis vehicula lectus ultricies eu. In convallis amet leo non sapien iaculis efficitur consequat lorem ipsum.</p>
						</div>
					</section>
					<section class="special">
						<ul class="icons labeled">
							<li><span class="icon solid fa-camera-retro"><span class="label">cada icone seus serviços</span></span></li>
							<li><span class="icon solid fa-sync"><span class="label">Sed vehicula elementum</span></span></li>
							<li><span class="icon solid fa-cloud"><span class="label">Elit fusce consequat</span></span></li>
							<li><span class="icon solid fa-code"><span class="label">Lorem nullam tempus</span></span></li>
							<li><span class="icon solid fa-desktop"><span class="label">Adipiscing amet sapien</span></span></li>
						</ul>
					</section>
				</div>
			</section>

		<!-- Three -->
			<section id="three" class="wrapper style2 special">
				<header class="major">
					<h2>Seu nome completo </h2>
					<p>Um pouco sobre você e depois insira novamente o pdf<br />
					com o seu curriculo para download.</p>
				</header>
				<ul class="actions special">
					<li><a href="#" class="button primary icon solid fa-download">Download</a></li>
					<li><a href="#" class="button">Learn More</a></li>
				</ul>
			</section>

		<!-- Footer -->
			<footer id="footer">
				<ul class="icons">
					<li><a href="#" class="icon brands fa-facebook-f"><span class="label">Facebook</span></a></li>
					<li><a href="#" class="icon brands fa-twitter"><span class="label">Twitter</span></a></li>
					<li><a href="#" class="icon brands fa-instagram"><span class="label">Instagram</span></a></li>
				</ul>
				<p class="copyright">&copy; Untitled. Credits: <a href="http://html5up.net">HTML5 UP</a> , <a href="#">Nascimento</a> </p>
			</footer>

{% endblock %}
```
**6.2-** Vá no navegador sua página ela tem que estar navegando normalmente. Caso apresente erro você colocou as escritas erradas ou a ordem de chamar os itens errada. O primeiro item a ser chamado é o extends, logo após é o load static e por ultimo é o block inicializando o bloco de conteudo. 
## 7- Criando componentes com Partials no Django:
**7.0-** Muita das vezes temos menus ou outra seção da nossa página que repitimos em outras páginas e isso não é uma boa pratica. Para solucionarmos esse problema precisamos criar componentes com esses blocos de código e chamar eles toda vez que necessario em nossas páginas, para isso utilizaremos o partials do python. No primeiro momento vamos criar uma pasta chamada "partials" dentro da nossa pasta template.<br>
**7.1-** Depois vamos criar dentro da pasta partials os arquivos footer.html e header.html e vou deixar os dois codigos ai para vocês verem:<br>
**footer.html**
```python
<footer id="footer">
    <ul class="icons">
        <li><a href="#" class="icon brands fa-facebook-f"><span class="label">Facebook</span></a></li>
        <li><a href="#" class="icon brands fa-twitter"><span class="label">Twitter</span></a></li>
        <li><a href="#" class="icon brands fa-instagram"><span class="label">Instagram</span></a></li>
    </ul>
    <p class="copyright">&copy; Untitled. Credits: <a href="http://html5up.net">HTML5 UP</a> , <a href="#">Nascimento</a> </p>
</footer>
```
**header.html**
```python
{% load static %}
<header id="header">
    <div class="content">
        <h1><a href="#">Igor Nascimento</a></h1>
        <p>Aqui você colocara um curriculo seu,<br />
        no formato de pdf para ser baixado</p>
        <ul class="actions">
            <li><a href="#" class="button primary icon solid fa-download">Download</a></li>
            <li><a href="#one" class="button icon solid fa-chevron-down scrolly">Learn More</a></li>
        </ul>
    </div>
    <div class="image phone"><div class="inner"><img src="{% static 'images/screen.jpg' %}" alt="" /></div></div>
</header>
```
**7.2-** Por último vamos incluir esses nosso novo componente em nosso arquivo index.html para fazermos essa inclusão usaremos o código {% include 'partials/nome_seu_arquivo' %} como vemos as imagens a seguir da inclusão do header e do footer:<br>
![header](https://github.com/IMNascimento/DjangoSenai/assets/28989407/5a7e71b8-62f4-4e97-95f3-cc2fdee72d4e)<br>
![footer](https://github.com/IMNascimento/DjangoSenai/assets/28989407/468922c1-5307-460b-88e9-3a80760621f4)<br>
**7.3-** Como vimos na imagem a cima marcado de vermelho os códigos utilizados no nosso index.html após a realização desse procedimento teste e verifique se sua aplicação continua carregando normalmente.<br>
## 8- Criando banco de dados e migrations no Django:
**8.0-** Já vimos que conseguimos mexer muito no nosso layout mas oque falta é deixar ele dinamico e então vamos criar um banco de dados para que todos os itens sejam cadastrado de forma dinamica pelo o usuário e retorne para os nossos templates para serem exibidos, nessa primeira parte nós instalaremos os modulos e criaremos as migrations.
<br>
**8.1-** Para usarmos o banco de dados mysql utilizaremos 2 modulos o mysql conector e o mysqlclient vou demonstrar o codigo de instalação dos mesmo para vocês:
```bash
(igor)C:\DjangoSenai\trilhas> pip install mysql-connector-python
(igor)C:\DjangoSenai\trilhas> pip install mysqlclient
```
**8.2-** Após vocês terem instalado os módulos vá no seu arquivo de configuração settings.py em database e coloque as informações do seu banco como veremos na imagem a seguir:<br>
![databaseconfig](https://github.com/IMNascimento/DjangoSenai/assets/28989407/14f4dc81-49cc-4703-92f5-c12b7e8cc12c)<br>
**8.3-** Depois de alterado vá no seu "APP" que foi criado no nosso caso aqui é o siteTrilhas e vá no arquivo models.py e la coloque o seguinte código:

```python
from datetime import datetime
from django.db import models

# Create your models here.
class Site(models.Model):
    nome_card = models.CharField(max_length=200)
    description =  models.TextField()
    path = models.TextField()
    primeiro_texto = models.TextField()
    segundo_texto = models.TextField()
    alunos = models.IntegerField()
    date_create = models.DateTimeField(default=datetime.now, blank =True)
```
**8.4-** Após essas ações executadas precisamos informa ao django para ele pegar nossa model e transformar em uma migration, para isso executaremos o comando makemigrations como veremos no exemplo a seguir:
```bash
(igor)C:\DjangoSenai\trilhas> python manage.py makemigrations
```
**8.5-** Assim que o comando foi executado agora vamos pedir ao django para criar nosso banco de dados. Com comando migrate, quando esse comando for executado o python executará e criará nossas tabelas no banco de dados, vejam o exemplo a seguir:
```bash
(igor)C:\DjangoSenai\trilhas> python manage.py migrate
```
**8.6-** Por último vá ao seu banco de dados e verifique se suas tabelas foram criadas com sucesso.

## 9 - Criando o Admin no Django:
**9.0-** Para poder utilizar um CRUD pronto do django devemos utilizar o modelo admin. Para isso precisamos de registrar nossos modelos, dentro do nosso app vamos verificar que existe um arquivo chamado admin.py vamos até ele e importaremos nosso modelo e registraremos o mesmo como veremos na imagem abaixo:<br>
![admindjango](https://github.com/IMNascimento/DjangoSenai/assets/28989407/04ffca60-0a08-4149-8a1d-0fcad53f2988)<br>
**9.1-** Agora devemos criar um super usuario para o django para isso iremos utilizar o seguinte comando no terminal:
```bash
(igor)C:\DjangoSenai\trilhas> python manage.py createsuperuser
```
**9.2-** A partir desse comando você deve digitar o nome do usuario e o email e senha de acesso. <br>
**9.3-** Agora teste a aplicação acesse o admin e cadastre um item no banco de dados.<br>



## Dicas:
**Criação de projetos como setup:**
- Ao criar projetos com o comando "django-admin startproject 'nome_do_projeto'", podemos colocar o nome do projeto como "setup".
- Assim, quando for criado, basta trocar o nome da pasta principal para o desejado.
- A estrutura ficará assim:
- ![djangosetupcodigo](https://github.com/IMNascimento/DjangoSenai/assets/160553204/17545d39-b212-4738-8f68-beb37a085d1f)
- ![djangosetup](https://github.com/IMNascimento/DjangoSenai/assets/160553204/9be8fd74-e296-42df-a060-d427fa36c65b)

**Replicação de ambientes:**
- Para replicar ambientes venvs vamos utilizar o modulo no python chamado freeze. Para que ele possa salvar em um arquivo txt todos os modulos e bibliotecas que utilizamos no projeto.
- Basta utilizar o comando "pip freeze > nome_arquivo.txt":
```bash
(igor)C:\python\Django> pip freeze > requeriments.txt
```
- Agora para você voltar e criar um servidor igual basta utilizar o comando "pip install -r nome_do_arquivo.txt"
```bash
(igor)C:\python\Django> pip install -r requeriments.txt
```
**Desativação de uma VENV:**
- Para desativar uma VENV basta apenas executar o comando "deactivate":
 ```bash
(igor)C:\python\Django> deactivate
C:\python\Django>
``` 
**Trocando nome da pasta de configurações:**
- No passo a passo lá em cima vemos que nossa pasta de configuração ela chama trilhas e depois de um periodo de desenvolvimento isso pode ficar confuso então caso você queira trocar o nome da pasta de configuração para setup para ficar melhor localizado basta apenas trocar alguns codigos de alguns arquivos, **obs:** não é muito recomendado que se faça essa ação no meio do projeto e sim no inicio de desenvolvimento.<br>
- Para realizarmos tal feito vou mostrar os arquivos que devem ser alterados que são o asgi.py, settings.py, wsgi.py, manage.py. Em cada arquivo desse vai ter links para pasta com o nome da sua pasta antiga basta trocar pelo nome da pasta nova, vou deixar os códigos já pronto para troca logo embaixo:<br>
- **asgi.py**
```python
"""
ASGI config for teste project.

It exposes the ASGI callable as a module-level variable named ``application``.

For more information on this file, see
https://docs.djangoproject.com/en/4.2/howto/deployment/asgi/
"""

import os

from django.core.asgi import get_asgi_application

os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'setup.settings')

application = get_asgi_application()

```
- **settings.py**
```python
"""
Django settings for teste project.

Generated by 'django-admin startproject' using Django 4.2.2.

For more information on this file, see
https://docs.djangoproject.com/en/4.2/topics/settings/

For the full list of settings and their values, see
https://docs.djangoproject.com/en/4.2/ref/settings/
"""

from pathlib import Path

# Build paths inside the project like this: BASE_DIR / 'subdir'.
BASE_DIR = Path(__file__).resolve().parent.parent


# Quick-start development settings - unsuitable for production
# See https://docs.djangoproject.com/en/4.2/howto/deployment/checklist/

# SECURITY WARNING: keep the secret key used in production secret!
SECRET_KEY = 'django-insecure-ojbqcmb5f5=z7bq3per1tss%82+lfj5n-w64u16*uof%vtm^tj'

# SECURITY WARNING: don't run with debug turned on in production!
DEBUG = True

ALLOWED_HOSTS = []


# Application definition

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
]

MIDDLEWARE = [
    'django.middleware.security.SecurityMiddleware',
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.middleware.common.CommonMiddleware',
    'django.middleware.csrf.CsrfViewMiddleware',
    'django.contrib.auth.middleware.AuthenticationMiddleware',
    'django.contrib.messages.middleware.MessageMiddleware',
    'django.middleware.clickjacking.XFrameOptionsMiddleware',
]

ROOT_URLCONF = 'setup.urls'

TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.debug',
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]

WSGI_APPLICATION = 'setup.wsgi.application'


# Database
# https://docs.djangoproject.com/en/4.2/ref/settings/#databases

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}


# Password validation
# https://docs.djangoproject.com/en/4.2/ref/settings/#auth-password-validators

AUTH_PASSWORD_VALIDATORS = [
    {
        'NAME': 'django.contrib.auth.password_validation.UserAttributeSimilarityValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.MinimumLengthValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.CommonPasswordValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.NumericPasswordValidator',
    },
]


# Internationalization
# https://docs.djangoproject.com/en/4.2/topics/i18n/

LANGUAGE_CODE = 'en-us'

TIME_ZONE = 'UTC'

USE_I18N = True

USE_TZ = True


# Static files (CSS, JavaScript, Images)
# https://docs.djangoproject.com/en/4.2/howto/static-files/

STATIC_URL = 'static/'

# Default primary key field type
# https://docs.djangoproject.com/en/4.2/ref/settings/#default-auto-field

DEFAULT_AUTO_FIELD = 'django.db.models.BigAutoField'
```
- **wsgi.py**
```python
"""
WSGI config for teste project.

It exposes the WSGI callable as a module-level variable named ``application``.

For more information on this file, see
https://docs.djangoproject.com/en/4.2/howto/deployment/wsgi/
"""

import os

from django.core.wsgi import get_wsgi_application

os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'setup.settings')

application = get_wsgi_application()

```
- **manage.py**
```python
def main():
    """Run administrative tasks."""
    os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'setup.settings')
    try:
        from django.core.management import execute_from_command_line
    except ImportError as exc:
        raise ImportError(
            "Couldn't import Django. Are you sure it's installed and "
            "available on your PYTHONPATH environment variable? Did you "
            "forget to activate a virtual environment?"
        ) from exc
    execute_from_command_line(sys.argv)


if __name__ == '__main__':
    main()

```
