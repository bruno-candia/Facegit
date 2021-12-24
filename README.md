``` javascript
import React, { useState } from 'react';

//Componente: Sempre com a primeira letra em maiúscula. Ele é uma função que retorna um conteúdo HTML, JSX, CSS, etc.
// ou pode se dizer que é um bloco isolado de HTML, CSS e JS o qual não interfere no restante do código.


//Propriedade: São informações que os componentes pais passam para os componentes filhos, 
//ou seja, os componentes filhos podem receber propriedades.

//Estado: Informação mantidas pelo componente. (Lembrar: Estado é imutável)


import Header from './Header';

// Componente: Sempre com letra maiúscula.
function App() {
  // useState: retorna um array com duas posições: o valor do estado e uma função para atualizar o valor do estado.
  const [counter, setCounter] = useState(0);

  function incrementCounter(){
    setCounter(counter + 1);
  }
  return (
    <>
      <h1>Contador: {counter}</h1>
      <button onClick={incrementCounter}> Incrementar</button>
      <Header title="Título" paragraph="Parágrafo" />
    </>
  );
}

export default App;
```