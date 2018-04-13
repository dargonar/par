# PAR

PAR es una implementacion de un [Sistema de Crédito Mutuo](https://en.wikipedia.org/wiki/Mutual_credit). 
En un sistema de crédito mutuo los miembros se dan crédito a través de la emisión de una moneda. La cantidad a emitir puede ser igual para todos, es decir se emite al misma cantidad a cada miembro, o se emite según la capacidad de producción de cada uno, ... o cualquier otro método. Esto significa que el método de asignación inicial es arbitrario.

### Asignación de crédito inicial
```
1. Igual para todos.
2. Representa un porcentaje de la capacidad productiva de un miembro.
3. Representa un porcentaje de los montos de venta mensuales promedio de un miembro.
4. Representa un porcentaje de la capacidad productiva de una actividad económica y es igual a todos lo de esa actividad.
5. X
```

### Emisión total
La implementación PAR de un SdCM tiene como objetivo poner una cantidad de dinero en circulación tal que refleje el total de productos y servicios comercializados, es decir que la suma de productos vendidos en un período de tiempo será el indicador de la cantidad de dinero en circulación.

#### Por qué dar crédito?
Dar crédito significa que un miembro decide incorporar al sistema a proveedores y consumidores otorgándoles un descubierto.

##### Cómo se emite?
Cuando un nuevo miembro se suma al sistema se le asigna un descubierto o crédito. Es es la manera general en que se emite en el sistema: con el ingreso de un nuevo miembro.

##### Emisión inicial
El nuevo miembro accede a un descubierto equivalente a un porcentaje configurable de ventas mensuales correspondientes a su rubro económico y a su capacidad de producción y venta. Dos productores de miel similares en producción y venta accederán a un mismo descubierto.

##### Corrección
Los miembros desarrollan su actividad económica y sus transacciones quedan registradas en el sistema. Cuando un miembro compra bienes y servicios en PARE$ en la comunidad significa que es la comunidad quien esta financiando al comprador. Cuando un miembro vende a alguien de la comunidad, es el miembro quien financia a la comunidad. 
Cada período de tiempo (inicialmente mensual) el sistema computa los montos transaccionados por cada miembro, y se ajusta con un coeficiente que involucra la consideración de la comunidad para con el miembro (a travś de un sistema de rating punto a punto por cada transaccion) disminuyendo o aumentando, según corresponda, el descubierto. El valor final del cómputo determina la **performance** del miembro en la comunidad. Aquellos miembros que hayan dado creédito a terceros, su **performance** reflejará tambi  ;en la **performance** de sus acreditados.

### Quiénes emiten?

##### 1er etapa: Comité
Un comité realizará el onboard de miembros y su respectiva emisión. 

##### 2da etapa: Comité + Agentes
El comité puede determinar agentes de crédito. 

##### 3er etapa: Comité + Agentes + High Performance Members
Miembros que tengan buena **performance** podrán otorgar créditos.

### Performance
Member's performance is a function of:
1. La integral de la curva de su balance en comparación con el descubierto
Si la integral es superior al área de su balance x periodo, quiere decir que el Member está financiando a la comunidad.
Si la integral es inferior al área de su balance * periodo, quiere decir que el Member está siendo financiado por la comunidad.
2. Cantidad y monto de transacciones realizadas en el perído.
Si A resulta satisfactorio, pero en el período realizó solo 1 TX por 5 pesos, no es un miembro que aporte valor ni tenga compromiso en el éxito del programa.
3. Rates
La comunidad se vota entre sí en cada interacción económica. El rate se tendrá en cuenta para computar la performance final.

### Parámetros del sistema
##### demurrage
Oxidación del dinero. Es un porcentaje que se licúa de cada tenedor mes a mes. Incentiva la actividad económica a través del gasto.
##### interest_rate
Incremento en la deuda en un porcentaje que se computa a mes vencido sobre el balance del miembro.
##### initial credit limits
Configuracion de créditos iniciales por tipo (A, B , C) o (Consumidor, Cuentapropista, Empresa)



