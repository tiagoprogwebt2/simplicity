```html
<!-- INÍCIO HTML PARA CEP/ENDEREÇO -->
        <div>
            <label for="cep">CEP: <br><span id="status"></span></label>
            <div id="area-do-cep">
                <!-- Usamos inputmode numerica para que
                o teclado virtual mostre números e para que não seja mostrado botões adicionais no navegador desktop. -->
                <input maxlength="9" inputmode="numeric" placeholder="Somente números" type="text" id="cep" name="cep" required> <br>
                <button id="buscar">Buscar</button>
            </div>
        </div>
        <div class="campos-restantes">
            <label for="endereco">Endereço:</label>
            <input type="text" id="endereco" name="endereco" size="30">
        </div>
        <div class="campos-restantes">
            <label for="bairro">Bairro:</label>
            <input type="text" id="bairro" name="bairro">
        </div>
        <div class="campos-restantes">
            <label for="cidade">Cidade:</label>
            <input type="text" id="cidade" name="cidade">
        </div>
        <div class="campos-restantes">
            <label for="estado">Estado:</label>
            <input type="text" id="estado" name="estado">
        </div>
<!-- /FIM HTML PARA CEP/ENDEREÇO -->
 ```

```css
#area-do-cep {
    display: flex;
    justify-content: space-between;
}

#cep { width: 50%; }

#buscar { 
    width: 49%;
    padding: 12px;
}

.campos-restantes { display: none; }
```


```javascript
/* Selecionando os elementos que serão manipulados */
const formulario = document.querySelector("form");
const campoCep = document.querySelector("#cep");
const campoTelefone = document.querySelector("#telefone");
const campoEndereco = document.querySelector("#endereco");
const campoBairro = document.querySelector("#bairro");
const campoCidade = document.querySelector("#cidade");
const campoEstado = document.querySelector("#estado");
const botaoBuscar = document.querySelector("#buscar");
const mensagemStatus = document.querySelector("#status");
```