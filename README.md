## bessel_functions
Bessel functions python routine plot

Si importano il modulo python per il calcolo numerico:

    import numpy as np

Dal modulo di calcolo scientifico si importa solo la funzione jv 

    from scipy.special import jv
    
che calcola il valore della funzione di Bessel i-esima nel punto x:

    jv(i,x)

Ad esempio pr i = 0 e x = 2 calcola J0(2) 

Si importa il modulo per tracciare le curve sul piano:

    import matplotlib.pyplot as plt

Si creano 10000 punti di calcolo tra 0 e 20 sull'asse x: 

    x = np.linspace(0, 20, 10000)

Si calcolano le prime 10 funzioni di Bessel su ogni valore di x e creo i grafici:

    for i in range(0, 10):
        J = jv(i, x)
        plt.plot(x, J, label=r'$J_' + str(i) + '(x)$')
        
Abbellisco i grafici introducendo una legenda, le etichette sugli assi e una griglia:

    plt.legend()
    plt.title('Bessel function', fontweight='bold', fontsize=10)
    plt.xlabel('mf', fontweight='bold', fontsize=10)
    plt.ylabel('$J_i(x)$', fontweight='bold', fontsize=16)
    plt.grid()

Rendo il grafico visibile:

    plt.show()

