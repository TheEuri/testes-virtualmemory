Esses testes são para ser rodados em ambiente linux. Se você estiver no windows, você pode usar o WSL (Windows Subsystem for Linux) para rodar esses comandos.

Primeiro, certifique-se de que o arquivo tem permissões de execução. Você pode fazer isso com o comando chmod:
`chmod +x run.sh`

Agora você pode rodar o script com o comando:
Se você quiser rodar todos os testes presentes na pasta de test, voce deve dar o seguinte comando:
`./run.sh all`

Caso queira executar um teste específico execute o seguinte comando:
`./run.sh [num_do_teste]`
ex.: `./run.sh 1`

Se houver diferenças no seu resultado ele printará esses erros na pasta diff com o nome do arquivo que deu a diferença.
Sendo a linha começando com `<` o recebido e a linha começando com `>` o resultado esperado.

**O SCRIPT NÃO MODIFICA NADA DO SEU CÓDIGO.** Ele apenas compila seu código e roda os testes. 

A pasta deve está organizada da seguinte forma:

```
.
├── Makefile
├── vm.c
├── BACKING_STORE.bin
├── run.sh
├── test
│   ├── 1
│   │   ├── addresses_1.txt
│   │   ├── addresses_1_fifo.txt
│   │   ├── addresses_1_lru.txt
│   ├── N
│   │   ├── addresses_N.txt
│   │   ├── addresses_N_fifo.txt
│   │   ├── addresses_N_lru.txt
```

Esses testes foram criados em conjuto por:
Eurivaldo Filho, Claudio Alves, Guilherme Cardoso, Pedro Lira, Igor Wanderley, Felipe Serpa e Gabriel Lima.

Nós geramos os arquivos de teste e rodamos em nossos códigos de forma a entrar em consenso sobre qual seria a resposta correta.

Desejamos boa sorte!

**Os testes 7 e 8 são coisa de maluco, 200 mil entradas, demora muito mesmo, por isso que não estão na pasta de testes, se quiser rodar eles basta coloca-los na pasta de test e rodar o comando `./run.sh [numero]` de forma unitária.**
