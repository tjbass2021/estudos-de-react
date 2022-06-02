# Introdução ao React

---

## Iniciando um projeto

Para inicializarmos um projeto com React, com o Node instalado, executamos o comando:

`npx create-react-app <nome-do-projeto>`

Assim, teremos ao final nosso projeto criado. Ao abrirmos o diretório do projeto via terminal e executarmos o comando `npm start`, teremos um servidor interno criado pelo Node, com a nossa aplicação ainda sem nenhuma alteração.

## Trabalhando com Bootstrap no React

Normalmente, para trabalharmos com a biblioteca React, incluímos o script do JQuery, o script do Bootstrap e a folha de estilo do Bootstrap em nosso `index.html`. Mas com React não é assim que funciona, pois não lidamos diretamente com o documento HTML de nosso projeto. Portanto, alguns passos deverão ser seguidos.

### Instalando o Bootstrap e depências

Para seu funcionamento, o Bootstrap necessita também do JQuery e do Popper, então instalamos todos estes módulos com o seguinte comando:

`npm install jquery popper bootstrap`

### Importando os módulos

Em nosso projeto, no diretório `src` criaremos o diretório `includes` que conterá os arquivos `jquery.js`, `popper.js` e `bootstrap.js`.

#### jquery.js

Dentro do arquivo 'jquery.js' inserimos o seguinte código:

~~~javascript
import * as $ from 'jquery'

window.jQuery = window.$ = $
~~~

#### popper.js

No arquivo do Popper, inseriremos o seguinte código:

~~~javascript
import Popper from 'popper.js'

window.Popper = Popper
~~~

#### bootstrap.js

Agora no arquivo `bootstrap.js` inseriremos o seguinte código:

~~~javascript
import './jquery'
import './popper'

import 'bootstrap'
import 'bootstrap/dist/css/bootstrap.min.css'
~~~

#### index.js

Por fim, ainda no diretório `src`, adicionaremos o seguinte código ao arquivo `index.js`:

~~~javascript
import './include/bootstrap'
~~~

