

### dia 01
anotações de js:
// variaveis
const msg = "Bem vinde"

// string => ``, '', ""
// number 2 1.3

// function
alert(msg)

---
 const atividade = {
  nome: 'almoço',
  data: new Date("2024-07-08 10:00"),
  finalizada: true
 } 

// lista, array
const atividades = [
  atividade, 
  {
    nome: 'academia em grupo',
    data: new date("2024-07-08"),
    finalizada: false
  },
    {
    nome: 'Gaming session',
    data: new date("2024-07-16 12:00"),
    finalizada: false
  },
      {
    nome: 'Jantar',
    data: new date("2024-07-16 16:00"),
    finalizada: true
  },
]


//arow functiom
const criarAtividade = (atividade) => { 

  // quando vai mudar pode usar let, assim não fica sempre a mesma coisa -> let change
  let input = '<input type="checkbox" '

  
  if(atividade.finalizada){
    input += 'checked'
  }

// += -> o mesmo concatena a mesma coisa dá no mesmo que usar input = input
  input += '>'
  
  return `
  <div>
      ${input}
      <span>${atividade.nome}</span>
      <time>${atividade.data}</time>
  </div>
  `
}

//document é um objeto, e querySelector é uma "tag" tipo button, section etc

// manipulando dados de html atraves do js
const section = document.querySelector('section')

for(let atividade of atividades){
  section.innerHTML =  criarAtividade(atividades)
}