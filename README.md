# Tecnologia Web Service e Restful<br>
<h1>Projeto simples de CRUD e integração client x server com tema Livraria</h1>
<h2>Utilização de XML e JSON para exemplificação desse estudo</h2>
<h3>Ferramentas utilizadas:</h3>
Spring Tools Suite 5<br>
Java 25<br>
Maven 3.9<br><br>

<h2><b>Foco:</b></h2>
<h3><i>Princípios Rest</i></h3>
<ul>
    <li>Identificação de recursos</li>
    <li>Utilização de métodos padronizados</li>
    <li>Múltiplas representações de recursos</li>
    <li>Comunicação sem estado</li>
    <li>Vinculação de recursos - HATEOAS</li>
</ul>

<h2><b>Métodos implementados no server:</b></h2>
<ul>
  <li>GET</li>
  <li>POST</li>
  <li>PUT</li>
  <li>DELETE</li>
</ul>

<h2><b>Métodos implementados no client:</b></h2>
<ul>
  <li>GET</li>
  <li>POST</li>
</ul>

<h2><b>URLs:</b></h2>
http://localhost:8080/livraria-virtual/livro/<br>
https://localhost:8443/livraria-virtual/livro/

<h2><b>Postman:</b></h2>
<i>OBS.: Quando testar com https, seguir conforme imagem para poder fazer autenticação:<img width="1159" height="281" alt="Captura de ecrã_2026-06-26_03-14-45" src="https://github.com/user-attachments/assets/1beb550d-e0c9-4f15-b68f-7dcc1ed71130" />
</i>
Método POST (xml):
<pre>
&lt;livro id="3"&gt;
    &lt;titulo&gt;Livro C&lt;/titulo&gt;
    &lt;isbn&gt;ISBN-9999&lt;/isbn&gt;
    &lt;genero&gt;Genero A&lt;/genero&gt;
    &lt;preco&gt;29.99&lt;/preco&gt;
    &lt;autor id="2"&gt;
        &lt;nome&gt;Autor 1&lt;/nome&gt;
    &lt;/autor&gt;
&lt;/livro&gt;
</pre>
Método POST (json):
<pre>
{
    &quot;autor&quot;: [
        {
            &quot;id&quot;: 2,
            &quot;nome&quot;: &quot;Autor 1&quot;
        }
    ],
    &quot;genero&quot;: &quot;Genero A&quot;,
    &quot;id&quot;: 3,
    &quot;isbn&quot;: &quot;ISBN-9999&quot;,
    &quot;preco&quot;: 99.99,
    &quot;titulo&quot;: &quot;Livro A&quot;
}
</pre>
<b>Gerado certificado com o keytool do proprio java para configurar um servidor ssl local jetty</b><br>
<i>(comando abaixo executado na raiz do projeto livraria-virtual)</i>:<br>
keytool -genkey -keyalg RSA -alias nome_alias -keystore server.keystore -storepass senha_store -validity 360 -keysize 2048
