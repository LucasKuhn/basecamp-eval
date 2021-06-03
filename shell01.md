# Shell01
#basecamp/evaluation

### ex00
- [ ] Se inscreveu no Exame00 - Evento
- [ ] Se inscreveu no Exame00 - Projeto

### ex01
> Escreva uma linha de comando que determine e mostre a lista de grupos dos quais o login especificado na variável de ambiente FT_USER é membro, separando-os por vírgulas sem espaços  

```sh
FT_USER=student ./print_groups.sh
# student,:,student,staff,main,basecamp,fortytwo$>
FT_USER=staff ./print_groups.sh
# staff,:,staff,god,main,bocal$>
```

### ex02
> Escreva uma linha de comando que procure na pasta atual e em todas as subpastas todos os arquivos cujos nomes terminam com “.sh”(sem as aspas) e que só exiba os seus nomes, sem o .sh.  

```sh
touch file.sh
touch shush
mkdir folder ; touch folder/subfile.sh
mkdir folder/subfolder ; mkdir folder/subfolder/subsubfile.sh

./find_sh.sh | cat -e
```

### ex03
> Escreva uma linha de comando que mostre o número de arquivos regulares e de pastas dentro da pasta atual e todas as suas subpastas, incluindo o “.”da pasta inicial.  

```sh
touch file
mkdir folder ; touch folder/subfile
mkdir folder/subfolder ; touch folder/subfolder/subsubfile
./count_files.sh | cat -e
# 7$
```

## ex04
> Escreva uma linha de comando que mostre os endereços MAC de sua máquina, respeitando o formato abaixo  
```sh
./MAC.sh | cat -e
# f2:5b:44:60:f5:aa$
# 8a:ec:c7:ac:30:81$
# ca:17:6b:da:36:fc$
# 02:42:0a:02:03:0a$
```

## ex05
> Crie um arquivo contendo somente “42”e NADA mais. * Ele deve ser nomeado: `“\?$*’MaRViN’*$?\”`  
```sh
ls -lRa *MaRV* | cat -e
# -rw---xr-- 1 75355 32015 2 Oct 2 12:21 "\?$*'MaRViN'*$?\"$
```

## ex06
> Escreva uma linha de comando que exiba um ls -l uma linha a cada duas (linha sim, linha não), a partir da primeira.  
```sh
touch file1 file2 file3 file4 file5
./skip.sh 
# total 4
# -rw-r--r-- 1 XX XX  0 Jun  3 00:13 file2
# -rw-r--r-- 1 XX XX  0 Jun  3 00:13 file4
# -rwxr-xr-x 1 XX XX 25 Jun  2 01:00 skip.sh
```

## ex07
> Escreva uma linha de comando que exiba a saída de um cat _etc_passwd, retirando os comentários, uma linha a cada duas começando pela segunda, invertendo cada login e ordenando em ordem alfabética inversa, mantendo apenas os logins compreendidos entre FT_LINE1 e FT_LINE2 inclusos, separados por “, “(sem aspas), e terminando com “.”.  
```sh
FT_LINE1=0 FT_LINE2=4 ./r_dwssap.sh
# yxorp,ydobon,XX,sys.$>
FT_LINE1=7 FT_LINE2=15 ./r_dwssap.sh
# pukcab, pl, nomead, mixe-naibeD, goltig, ffats, evloser-dmetsys, cri, cnysemit-dmetsys.$>
```

## ex08
> Escreva uma linha de comando que pegue os números contidos nas variáveis FT_NBR1 de base ’\”?! e FT_NBR2 de base mrdoc, e que também exiba a soma dos dois em base gtaio luSnemf (sim, o espaço conta)  
```sh
FT_NBR1="\\'?\"\\\"'\\" FT_NBR2=rcrdmddd bash add_chelou.sh
# Salud

FT_NBR1="\\\"\\\"\!\\\"\\\"\!\\\"\\\"\!\\\"\\\"\!\\\"\\\"\!\\\"\\\"" FT_NBR2=dcrcmcmooododmrrrmorcmcrmomo bash add_chelou.sh
# segmentation fault (?) or SfauggmuttnfnoemmSaml
```

