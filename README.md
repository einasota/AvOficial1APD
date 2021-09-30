# Utilizando OpenMP no Linux
### Instalação pelo Ubuntu.

É necessária a instalação de um compilador compatível com com OpenMP. Nesse tutorial estaremos utilizando o GCC.

No termina, execute os seguintes comandos:
```
sudo apt-get update
sudo apt-get install build-essential libomp-dev gcc-multilib
```
Após a instalação verifique se o OpenMP está configurado:`echo |cpp -fopenmp -dM |grep -i open` deve sair algo parecido com a imagem a baixo, se não verifique se a instalação ocorreu normalmente:

![Terminal Verificação](https://i.imgur.com/Cv7WGaG.png)

Depois devemos configurar a quantidades de threads que serão utilizadas:

    export OMP_NUM_THREADS=4

Após esses processos, possuindo um arquivo pronto para compilar, execute o seguinte comando: 

    gcc -o novonome -fopenmp nomedoarquivo.c
E para executar rode:

    ./novonome

Em conjunto com esse README.md existe um arquivo chamado Hello World. Execute o seguinte comando:
`gcc -o helloworld -fopenmp HelloWorld.c` e depois: `./helloworld`. 