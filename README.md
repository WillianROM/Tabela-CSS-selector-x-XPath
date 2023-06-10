<table>
    <tr>
        <th>Descrição</th>
        <th>CSS Selector</th>
        <th>XPath</th>
    </tr>
    <tr>
        <td>Todos os elemtentos</td>
        <td>*</td>
        <td>//*</td>
    </tr>
    <tr>
        <td>Um elemento</td>
        <td>tag</td>
        <td>//tag</td>
    </tr>
    <tr>
        <td>Identificando todos os elementos filhos de uma tag</td>
        <td>tag *</td>
        <td>//tag//*</td>
    </tr>
    <tr>
        <td>Muitos elemento</td>
        <td>tag1, tag2</td>
        <td>//tag1 | //tag2</td>
    </tr>
    <tr>
        <td>Selecionar pelo ID</td>
        <td>#value</td>
        <td>//tag[@id="valor"]</td>
    </tr>
    <tr>
        <td>Selecionar pela classe</td>
        <td>.value</td>
        <td>//tag[@class="valor"]</td>
    </tr>
    <tr>
        <td>Um atributo de um elemento deve ser exatamente igual</td>
        <td>tag[atributo='valor']</td>
        <td>//tag[@atributo='valor']</td>
    </tr>
    <tr>
        <td>Um elemento que NÃO tenha determinado atributo</td>
        <td>tag:not([atributo="valor"])</td>
        <td>//tag[not(@atributo="valor")]</td>
    </tr>
    <tr>
        <td>Um atributo de um elemento deve conter</td>
        <td>tag[atributo*='valor']</td>
        <td>//tag[contains(@atributo, 'valor')]</td>
    </tr>
    <tr>
        <td>Um atributo de um elemento deve começar com</td>
        <td>tag[atributo^='valor']</td>
        <td>//tag[starts-with(@atributo, 'valor')]</td>
    </tr>
    <tr>
        <td>Um atributo de um elemento deve terminar com</td>
        <td>tag[atributo$='valor']</td>
        <td>//tag[ends-with(@atributo, 'valor')]</td>
    </tr>
    <tr>
        <td>Um atributo de um elemento deve ser exatamente igual ou iniciar com</td>
        <td>tag[atributo|='valor']</td>
        <td>//tag[@atributo='valor' or starts-with(@atributo, 'val')]</td>
    </tr>
    <tr>
        <td>Um atributo de um elemento deve ser exatamente igual</td>
        <td>tag[atributo~='valor']</td>
        <td>//tag[contains(concat(' ', normalize-space  (@atributo), ' '), ' value ')]</td>
    </tr>
    <tr>
        <td>Identificando o primeiro tag filho</td>
        <td>tag>tag-filho:first-child</td>
        <td>(//tag/tag-filho)[1]</td>
    </tr>
    <tr>
        <td>Identificando o último tag filho</td>
        <td>tag>tag-filho:last-child</td>
        <td>(//tag/tag-filho)[last()]</td>
    </tr>
    <tr>
        <td>Identificando uma tag filho específico</td>
        <td>tag > tag-filho:nth-child(3)</td>
        <td>(//tag/tag-filho)[3]</td>
    </tr>
    <tr>
        <td>Hierarquia dos elementos para encontrar em qualquer parte das tags descendentes</td>
        <td>tag tag-descendente</td>
        <td>//tag//tag-descendente</td>
    </tr>
    <tr>
        <td>Hierarquia direto dos elementos para encontrar tags filhos logo abaixo da tag</td>
        <td>tag > tag-filho</td>
        <td>//tag/tag-filho</td>
    </tr>
    <tr>
        <td>Identificando elementos irmãos adjacente posterior</td>
        <td>tag[atributo="valor"] + tag-irmao</td>
        <td>//tag[@atributo="valor"]/following-sibling::tag-irmao</td>
    </tr>
    <tr>
        <td>Identificando elementos irmãos posterior, que estão no mesmo nível</td>
        <td>tag[atributo="valor"] ~ tag-irmao</td>
        <td>//tag[@atributo="valor"]/following-sibling::tag-irmao</td>
    </tr>
    <tr>
        <td>Somente XPath - Identificando elemento irmão anterior</td>
        <td></td>
        <td>//tag[@name="valor"]/preceding-sibling::tag-irmao</td>
    </tr>
    <tr>
        <td>Somente XPath - Identificando elementos pelo texto</td>
        <td></td>
        <td>//tag[text()='texto']</td>
    </tr>
    <tr>
        <td>Somente XPath - Identificando elementos que contém texto</td>
        <td></td>
        <td>//tag[contains(text(),'Parte do texto ou o texto completo')]</td>
    </tr>
    <tr>
        <td>Somente XPath - Identificando elementos filhos que contém texto, inves de usar text(), usasse .</td>
        <td></td>
        <td>//tag[contains(.,'Parte do texto ou o texto completo')]</td>
    </tr>
    <tr>
        <td>Somente XPath - Identificando elementos que NÃO contém um determinado texto</td>
        <td></td>
        <td>//tag[not(contains(text(),'Parte do texto ou o texto completo'))]</td>
    </tr>
    <tr>
        <td>Identificando algum elemento ancestral (pai, avô,...)</td>
        <td>tag-ancestral:has(tag[atributo="valor"])</td>
        <td>//tag[@atributo="valor"]/ancestor::tag-ancestral</td>
    </tr>
    <tr>
        <td>Somente XPath - Identificando o elemento pai direto informando a tag do elemento pai</td>
        <td></td>
        <td>//tag[@atributo="valor"]/parent::tag-pai</td>
    </tr>
    <tr>
        <td>Somente XPath - Identificando o elemento pai direto informando a tag do elemento pai - Outra forma</td>
        <td></td>
        <td>//tag-pai[./tag[@atributo="valor"]]</td>
    </tr>
    <tr>
        <td>Somente XPath - Identificando o elemento pai direto sem informar a tag do elemento pai</td>
        <td></td>
        <td>//tag[@atributo="valor"]/..</td>
    </tr>
    <tr>
        <td>Somente XPath - Utilize 'and' para colocar mais de uma condição para encontrar o elemento, no exemplo a tag contém determinado atributo e tem um tag filho com outro atributo</td>
        <td></td>
        <td>//tag[@atributo="valor" and ./tag-filho[@atributo='valor']]</td>
    </tr>
        <tr>
        <td>Somente XPath - também é possível usar 'or' quando se quer pegar elementos com a mesma tag em diferentes condições</td>
        <td></td>
        <td>//tag[@atributo="valor" or ./tag-filho[@atributo='valor']]</td>
    </tr>

    
</table>