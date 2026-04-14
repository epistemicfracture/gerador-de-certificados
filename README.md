<h1>Gerador de Certificados Simples (Google Colab)</h1>

<p>
Este repositório permite gerar certificados automaticamente em PDF a partir de uma lista de participantes em Excel.
O processo é executado diretamente no <strong>Google Colab</strong>, sem necessidade de instalar Python localmente.
</p>

<h2>Arquivos do repositório</h2>

<p>O repositório já contém:</p>

<ul>
  <li><strong>Gerador_de_certificados_simples.ipynb</strong> → notebook principal</li>
  <li><strong>Lista.xlsx</strong> → planilha modelo com nomes e e-mails</li>
  <li><strong>PDF do certificado</strong> → deve ser enviado no momento da execução no Colab</li>
</ul>

<h2>O que o script faz</h2>

<ol>
  <li>Lê os nomes da planilha Excel</li>
  <li>Insere o texto no certificado</li>
  <li>Gera um PDF final com todos os certificados</li>
  <li>Cria um arquivo com os e-mails dos participantes</li>
</ol>

<h2>Como usar no Google Colab</h2>

<h3>1. Abra o notebook</h3>
<p>
Abra o arquivo <strong>Gerador_de_certificados_simples.ipynb</strong> no Google Colab.
</p>

<h3>2. Execute o notebook</h3>
<p>
No menu do Colab, clique em <strong>Executar tudo</strong> ou use <strong>Ctrl + F9</strong>.
As bibliotecas necessárias serão instaladas automaticamente.
</p>

<h3>3. Envie a planilha</h3>
<p>
Quando o Colab solicitar a planilha, envie o arquivo:
</p>

<pre><code>Lista.xlsx</code></pre>

<p>A planilha deve conter exatamente estas colunas:</p>

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>E-mail</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>João da Silva</td>
      <td>joao@email.com</td>
    </tr>
  </tbody>
</table>

<h3>4. Envie o PDF modelo do certificado</h3>
<p>
Depois, o Colab solicitará o arquivo PDF que será usado como modelo de fundo do certificado.
Envie esse arquivo normalmente.
</p>

<h3>5. Baixe os arquivos gerados</h3>
<p>Ao final, serão gerados automaticamente:</p>

<ul>
  <li><strong>certificados_ouvintes.pdf</strong></li>
  <li><strong>emails_ouvintes.txt</strong></li>
</ul>

<h2>Como editar o texto do certificado</h2>

<p>
No notebook, procure a função <strong>montar_texto_certificado(nome)</strong>.
É nela que você pode alterar:
</p>

<ul>
  <li>nome do evento</li>
  <li>data</li>
  <li>local</li>
  <li>carga horária</li>
</ul>

<h2>Como ajustar a posição do texto</h2>

<p>
Se o texto aparecer muito alto, muito baixo ou fora do lugar no certificado, ajuste a variável:
</p>

<pre><code>TEXT_BOX_Y = 300</code></pre>

<p>Você pode testar valores como:</p>

<pre><code>TEXT_BOX_Y = 350
TEXT_BOX_Y = 300
TEXT_BOX_Y = 250
TEXT_BOX_Y = 200</code></pre>

<h2>Problemas comuns</h2>

<h3>O texto não aparece no certificado</h3>
<ul>
  <li>Verifique se o PDF enviado é o modelo correto</li>
  <li>Confirme se a planilha possui as colunas <strong>Nome</strong> e <strong>E-mail</strong></li>
  <li>Ajuste o valor de <strong>TEXT_BOX_Y</strong></li>
</ul>

<pre><code>Nome
E-mail</code></pre>

<h2>Licença</h2>

<p>CC0 1.0 Universal</p>
