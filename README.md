# Automatizando a Alteração de Tamanho de Fotos com PyAutoGUI

## Descrição do Projeto </h1>
Neste projeto, criei uma automação utilizando a biblioteca PyAutoGUI do Python para otimizar o processo de diminuição do tamanho de imagens em um e-commerce que utiliza a plataforma TRAY. A plataforma exige que as fotos carregadas tenham menos de 350 kB. Antes dessa automação, esse processo era realizado manualmente, o que consumia muito tempo e reduzia a produtividade.

Ao rodar o script, o código automatiza uma série de cliques e entradas para alterar o tamanho das imagens de maneira rápida e eficiente, reduzindo o trabalho manual. Durante os testes, consegui automatizar o processo para mais de 200 imagens de uma vez. Mesmo com a desvantagem de não poder utilizar o computador enquanto o script está em execução, a automação reduz significativamente o tempo do processo, permitindo que eu me dedique a outras tarefas enquanto o trabalho é feito no computador.

Funcionalidade:
* Redução do tamanho das imagens para menos de 350 kB.
* Automação do processo de carregamento, alteração e renomeação das imagens na plataforma TRAY.
* Capacidade de realizar várias repetições de forma rápida, poupando horas de trabalho manual.

Embora a biblioteca PyAutoGUI não permita que o computador seja utilizado enquanto o script está rodando, a automação compensa essa limitação ao realizar o trabalho de forma mais eficiente. Isso permite que eu possa realizar outras atividades enquanto o processo ocorre.

## Tecnologia:
Os softwares utilizados neste projeto foram:

* Jupyter Anaconda
* Python
* Galeria de imagens


## Serviço usado:
* Github


## Biblioteca Python:
* PyAutoGUI

## Script:

import pyautogui as pg
import time

repeticoes = 201

for i in range(repeticoes):
    print(f"Iniciando repetição {i + 1} de {repeticoes}...")
    time.sleep(1)

    pg.click(x=-1018, y=24)
    time.sleep(0.5)

    for seta_baixo in range(4):
        pg.press('down')

    pg.press('enter')
    time.sleep(0.5)

    for tab in range(2):
        pg.press('tab')
    time.sleep(1)

    for delete in range(4):
        pg.press('del', interval=0.2)

    pg.write('800', interval=0.2)
    pg.press('tab')

    for delete in range(4):
        pg.press('del', interval=0.2)

    pg.write('800', interval=0.2)

    for tab in range(3):
        pg.press('tab')
        time.sleep(0.3)
    
    pg.press('enter')
    time.sleep(2)

    pg.click(x=-381, y=49)
    time.sleep(0.3)

    pg.press('backspace')
    time.sleep(0.3)

    pg.write(r'C:\Users\Matheus\Documents\analises\maiah\python\pyautogui\tamanho alterado')
    time.sleep(0.3)

    pg.press('enter')
    time.sleep(0.3)

    pg.click(x=-799, y=625)

    008ve para a direita para ajustar o nome
    pg.press('right')
    time.sleep(0.3)

    pg.write('_tray')

    pg.click(x=-167, y=699)
    time.sleep(2)

    pg.press('right')
    time.sleep(0.5)    
    
    print(f"Repetição {i + 1} concluída.\n")
   

print("Todas as 201 repetições foram concluídas!")

## Autor
**Matheus Bonfim do Prado**: @bonfimdoprado (https://github.com/bonfimdoprado)
