# SpecialRewards
TP2_Cotta_Mikiej_Perl_Estray

Sub - producto o mejora:
Como hoy por hoy el TVL del protocolo es bastante bajo y se encuentra estancado, creemos que la mejor forma de potenciar el protocolo sería tratando de resolver ese problema. Es lógico pensar que existe un exceso de demanda de fondos por parte de organizaciones y usuarios en la blockchain, por lo que si el protocolo fuese capaz de proveer de mayor cantidad de liquidez a estos usuarios, entonces su TVL y popularidad aumentarían.
Sin embargo, no solo se requiere de usuarios para que el protocolo explote, sino también de backers o LP que sumen fondos a los Borrowers Pools para que los usuarios puedan fondearse. Por ende, creemos que el foco de la mejora debería implementarse en esta parte del protocolo y pensamos que la mejor manera de sumar backers y LP es aumentando los incentivos para que ellos aporten a Goldfinch.
Entonces pensamos en un sistema de bonos pagos en GFI llamado “Special Rewards” que basicamente aumentará el incentivo tanto de los LP como de los backers de proveer fondos.
Su funcionamiento consistirá de la siguiente manera:

Función 1: Cada vez que un backer o LP provea liquidez, se va a chequear su balance de fondos prestados al protocolo. Al llamar a la función te dice el balance del inversor.

Función 2: Si puso más de una cantidad determinada de fondos en USDC (definida por la gobernanza del protocolo), se va a activar un mensaje que le avisa al usuario que puede claimear sus GFI. Si el inversor no llega a los fondos necesarios, se le envía un mensaje avisando cuantos fondos le faltan para llegar a claimear la recompensa y lo incentiva a poner más dinero.

Función 3: Luego, el inversor podrá claimear sus GFI que se enviarán directo a su cuenta.

La feature de Special Rewards va a estar conectada con el front end a través de un contrato poríferico y le va a hacer la experiencia al inversos mucho más simple que llamando código. Basicamente, la función 1 la van a poder llamar mediante un boton y ver su balance, la 2 les va a aparecer automaticamente al aportar su dinero y la 3 les va a mandar el dinero automaticamente sin aparecer en el front.

Lo agregaríamos como un contrato core que aparezca en la interfaz de cada inversor al aportar liquidez.

Finalmente, usaríamos el lenguaje Solidity exclusivamente para programar este contrato. Si bien también podría pensarse en python para hacerlo más simple y de alguna manera migrarlo a la blockchain, creemos que es lo suficientemente simple para prograrmarlo en Solidity. No necesitamos otra tecnología adicional al smart contract.

