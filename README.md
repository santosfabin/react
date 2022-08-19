# REACT

Created: August 12, 2022 8:39 AM
Property: biblioteca
Type: JavaScript

- ReactJS não é um framework
    - Porque ele não tem uma opinião forte, ele não tem uma estrutura de pastas e regras que os frameworks em si tem. Ele te dá mais liberdade para criar as interfaces da maneira que preferir.
    - E sim uma biblioteca JavaScript que tem o objetivo de criação de interfaces.
    - Tudo é JavaScript, mas temos funções retornando conteúdo HTML
- Composição
    - SPA
        - Single Page Application
        - uma única página html
        - modelo atual
    - O react reescreve tudo que tiver dentro da div root
    - Então toda a aplicação ficará dentro dessa div
    - “dev”: “vite”,
        - script de inicialização
        - `npm run dev`
    
    `node_modules` - A pasta onde ficam todas dependências e módulos do nosso projeto.
    
    `src` - Pasta principal onde ficará todos os nossos arquivos.
    
- Site ReactJS
    
    <aside>
    ⚠️ [https://reactjs.org](https://reactjs.org/)
    
    </aside>
    
- VITE
    
    <aside>
    ⚠️ [https://vitejs.dev](https://vitejs.dev/)
    
    </aside>
    
    - No terminal
    
    ```bash
    npm create vite@latest
    ```
    
    - ou
    
    ```bash
    										//nome do projeto
    npm create vite@latest reactapp --template react
    ```
    
    - Dentro da pasta do projeto (reactapp)
    
    ```bash
    npm install
    ```
    
    - Usando
    
    ```bash
    npm run dev
    ```
    
- Configurando ambiente
    - Apagar
        - public
        - `<link rel=”icon” […]>`
        - assets (foulder) dentro do src
        - arquivos css dentro do src
        - Apagar as importações css
        - Dentro de App.tsx
            - Pode apagar todas as importações dentro dele
            - Pode apagar tudo para deixar dessa forma
            
            ![Untitled](REACT%20db0d7e1fe39942e683319888186194bf/Untitled.png)
            
    - Deixar
        - Obrigatório
            - vite-end.d.ts
        - App.tsx
        - main.tsx
    - scr:
        - Core
        - Aplicação em si
        - Fora dele é arquivos obrigatórios
        - Onde ficará todo o conteúdo
    - .ignore
        - não tirar nada de dentro, apenas adicionar
- Extensão
    - `.jsx`
        - Sintaxe para escrever html no javascript
        - É uma extensão do JavaScript bem semelhante ao HTML. Basicamente ele é uma sintaxe que o ReactJS utiliza para que possamos criar as nossas interfaces de forma declarativa.
        - O JSX utiliza funções dentro dos arquivos e o retorno dessas funções retornam tags
    - `.ts`
        - TypeScript
    - `.tsx`
        - TypeScript com `.jsx`
- export default
    - Deverá ser passado ao fim da função da seguinte maneira
    
    ```jsx
    function FazerBolor() {
    	return (
    		[...]
    	)
    }
    export default FazerBolo
    ```
    
    - Na hora do import na página que será usada
    
    ```jsx
    import FazerBolo from 'diretorio'
    ```
    
- export
    - Deverá ser passado o `export` nates antes da palavra `function`
    
    ```jsx
    export function FazerBolo() {
    	return(
    		[...]
    	)
    }
    ```
    
    - Na importação deverá ser passado o nome exato da `function` e entre `{ }`
    
    ```jsx
    import {FazerBolo} from 'diretorio'
    ```
    

---

- Projeto
    - O projeto sempre ficará dentro da `div.root`
    - Deverá ser feito `import nameFunction from ‘dirotory’` para a utilização do mesmo ao início do projeto
    - `main.jsx` é em poucas palavras o outro index
        - onde ficará seu conteúdo exportado
        
        ![Untitled](REACT%20db0d7e1fe39942e683319888186194bf/Untitled%201.png)
        
- Fragment
    - No elemento `.jsx` deve ser retornado apenas um elemento
    - Então para isso temos duas soluções
        - `<>` `</>`
            - no início e no fim
            
            ![Untitled](REACT%20db0d7e1fe39942e683319888186194bf/Untitled%202.png)
            
        - `<tag>`
            - É possível fazer isso embrulhando com alguma tag
            - Sendo ela uma `<div>`, `<section>`
- Importando CSS
    - Para importar não é necessário do `from` então basta fazer da seguinte forma
    
    ```jsx
    import './diretorio/arquivo.css'
    ```
    
    - Repare que deve sempre colocar sua extensão, no caso `.css`
    - Ela poderá ser colocado em qualquer lugar, portanto que corresponda com deu desejo
- Organizando páginas
    - Resultado
        
        ![Untitled](REACT%20db0d7e1fe39942e683319888186194bf/Untitled%203.png)
        
    - Basicamente é dividido cada componente em pasta separada com o nome do que ela significa
    - Então é feito um style global para limpar o default padrão do navegador

---

- Palavras reservadas
    - `className`
        - SEMPRE que estiver colocando o `class` no react, deve ser colocado no lugar `className`
        - Por quê?
            - Porque `class` é uma palavra reservada
    - `htmlFor`
        - Substitui o `for` do `label`

---

- Componentes
    - Componente nada mais do que um bloco de código reutilizável e independente.
    - Normalmente separamos por pastas cada componentes
    - Agrupando todos os componentes em uma pasta
    - Criando
        - Crie uma pasta com o nome do elemento
        - Dentro da pasta crie um `index.jsx` e um `style.css`
            - Essas serão as bases para o componente
        - No `index.jsx` importaremos o arquivo `.css`
            
            ```jsx
            import './style.css'
            ```
            
        - Sintaxe
            
            ```jsx
            import [...]
            export function Card() {
            	return(
            		<>
            			[...]
            		</>
            	)
            }
            ```
            
    - Usando
        - No arquivo que deseja colocar o componente
        - Primeiro o import
        
        ```jsx
        import { Card } from 'diretory'
        ```
        
        - Usar
        
        ```jsx
        <Card />
        //ou
        <Card></Card>
        ```
        
- Propriedades
    - Colocando propriedades
    - Em seu componente colocado é possível passar propriedades
        
        ![Untitled](REACT%20db0d7e1fe39942e683319888186194bf/Untitled%204.png)
        
    - Na pasta do seu componente é possível acessa-lo de duas formas
        - Parâmetro (pegando todos)
            - Basta passar um nome no parâmetro da `function()`
            - Depois é so pegar pelo objeto
                
                ![Untitled](REACT%20db0d7e1fe39942e683319888186194bf/Untitled%205.png)
                
        - Parâmetro (pegando um por um)
            - Ao invés de passar um nome de parâmetro, passe o nome das propriedades
            - Então não será preciso acessar pelo objeto, mas sim coloca-lo diretamente
                
                ![Untitled](REACT%20db0d7e1fe39942e683319888186194bf/Untitled%206.png)
                
        - Parâmetro (com variáveis)
            
            ```jsx
            export function Card(props) {
            	const textInserido = props.name
            	const textEmCapsLock = textoInserido.toUpperCase()
            	return <div>
            			{textoEmCapsLock}
            		</div>
            }
            ```
            
- Parentesco
    
    ![Untitled](REACT%20db0d7e1fe39942e683319888186194bf/Untitled%207.png)
    
    - A indentação, parentesco, filhos, são elementos um dentro do outro, então isso que iremos usar para usar tags html de modo semelhante a tag `<strong>`
    
    ```jsx
    export function Card(props) {
    	const textInserido = props.children
    	const textEmCapsLock = textoInserido.toUpperCase()
    	return <div>
    			{textoEmCapsLock}
    		</div>
    }
    ```
    

---

- `onChange`
    - Executará sempre que há atualização
    - Ele pode retornar `events` do próprio `onChange`
    - Um deles é o `target`, que é o próprio elemento de onde ele está
        - é bom para economizar tempo e código, pois ao invez de fazer `document.querySelector(…)…`use o `target`
    - Dele você pode pegar o `value` do elemento
    - Exemplo
        
        ```jsx
        <input onChange={ e => {
        	console.log(e.target.value)
        }}/>
        ```
        

---

- Imutabilidade
    - O conteúdo da variável não deve ser modificado e sim substituído.
    
    ```jsx
    import React, { useState } from 'react';
    
    import './styles.css';
    import { Card } from '../../componentes/Card';
    
    export function Home() {
      const [studentName, setStudentName] = useState('');
      const [students, setStudents] = useState([]);
    
      function handleAddStudent() {
        const newStudent = {
          name: studentName,
          time: new Date().toLocaleTimeString('pt-br', {
            hour: '2-digit',
            minute: '2-digit',
            second: '2-digit',
          }),
        };
    
        setStudents((prevState) => [
          //despejando o vetor pra ai dentro, então todo mundo fica no mesmo vetor
          ...prevState,
          newStudent,
        ]);
      }
    
      return (
        <div className="container">
          <h1>Nome: {studentName}</h1>
          <input
            type="text"
            placeholder="Digite o nome..."
            onChange={(e) =>
              setStudentName(e.target.value)
            }
          />
          <button type="button" onClick={handleAddStudent}>
            Adicionar
          </button>
    
          {students.map((student) => (
            <Card
              name={student.name}
              time={student.time}
            />
          ))}
        </div>
      );
    }
    ```
    
- Key
    - Em uma listagem, normalmente utilizamos o `map()` do JavaScript para trazer todos os dados dessa lista. No React, precisamos passar uma propriedade `key` para que esse dado nunca se repita e evitar que erros desse tipo aconteçam.
    
    ```jsx
    <Card
      key={student.time}
      name={student.name}
      time={student.time}
    />
    ```
    
- Hooks
    - São funções que permitem conectar os recursos de estados e ciclos de vida do React a partir de componentes funcionais. Normalmente os Hooks iniciam com a palavra `use` por convenção. Exemplos de hooks: `useState`, `useEffect`.
    
    <aside>
    ⚠️ [https://reactjs.org/docs/hooks-reference.html](https://reactjs.org/docs/hooks-reference.html)
    
    </aside>
    
    - [useState()](REACT%20db0d7e1fe39942e683319888186194bf.md) (version 2.0),(Hook)
        - O React não sabe quando atualizar os elementos, então por isso usamos o `useState()`
        - Então o `useState()` reflete renderizando nos componentes que o usam de acordo com usa alteração
        - Então no React vamos importar o useState
            
            ```jsx
            import { useState } from 'react';
            ```
            
        - Ele pode iniciar ou não com um valor
        - O `useState()` retorna um array
        - Sintaxe
            
            ```jsx
            const [contador, setContador] = useState(1)
            ```
            
            - [ (estado em si onde vai ficar armazenado), (função que atualiza o estado) ] = useState(’Valor Inicial / Pode ser deixado em branco sem aspas’)
        - Então para usar você deve passar para o segundo valor o que deve ser modificado
        - E o primeiro valor é o modificado
        - Exemplo
        
        ```jsx
        import { Box } from './style.js';
        import { useState } from 'react';
        
        export function Header() {
          const [contador, setContador] = useState(1);
        
          function addContador() {
            setContador(contador + 1);
          }
          return (
            <header>
                <div>{contador}</div>
              <button onClick={addContador}>
                ADICIONAL
              </button>
            </header>
          );
        }
        ```
        
        ---
        
        - Exemplo com input
            
            ```jsx
            import { useState } from 'react';
            
            export function Header() {
              const [contador, setContador] = useState();
            
              return (
                <header>
                  <div>Elemento: {contador}</div>
                  <input
                    type="text"
                    onChange={(e) => {
                      setContador(e.target.value);
                    }}
                  />
                </header>
              );
            }
            ```
            
    - useEffect
        - O `useEffect` é executado automaticamente sempre que o componente é renderizado.
        - Não é possível fazer ela como assincrono
        
        ```jsx
        useEffect(() => {
            //executa assim que for chamado
            console.log('Foi chamado');
          }, [
            //quando vazio vai ser executado apenas uma vez, quando a interface carregar
            //caso coloque um estado, sempre q esse estado for carregado ele será chamado
            students,
        		//pode ser colocado mais pós virgula, então quando algum deles mudar, será chamado
          ]);
        ```
        
- Resultado
    
    <aside>
    ⚠️ [https://github.com/santosfabin/Estudos/tree/main/React](https://github.com/santosfabin/Estudos/tree/main/React)
    
    </aside>