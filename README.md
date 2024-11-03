# Aula de Tratamento de Exceções em Java - Resumo da aula

- Solução 1  (muito ruim): lógica de validação no programa principal.
- Solução 2 (ruim): método retornando string
  - A semântica da operação é prejudicada
    - Retornar string não tem nada a ver com atualização de reserva
    - E se operação tivesse que retornar uma string ?
  - Ainda não é possível tratar exceções com construtores
  - Ainda não há auxílio do compilador: o programador deve "lembrar" de verificar se houve erro.
  - A lógica fica estruturada em condicionais aninhadas

- Solução 3 (boa): tratamento de exceções
  - cláusula throws: propaga a exceção ao invés de tratá-la
  - cláusula throw: lança a exceção / "corta" o método
  - Exception : compilador obriga a tratar ou propagar
  - RuntimeException: compilador NÃO obriga

- O modelo de tratamento de exceções permite que erros sejam tratados de forma consistente e flexível, usando boas práticas
  - Vantagens:
    - lógica delegada
    - construtoresm podem ter tratamento de exceções
    - possibilidade de auxílio do compilador (Exception)
    - Código mais simples. Não há aninhamentos dee condicionais: a qualquer momento que uma exceção for disparada, a execução é interrompida e cai no bloco catch correspondente
    - É possivel capturar inclusive outras exceções do sistema
