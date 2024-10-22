## JavaScript

### Identificadores:
  Son para identificar variables, funciones, clases y demás. Estos tienen algunas reglas y convenciones importantes.

#### Reglas Básicas:
	- Deben empezar con una letra, un guion bajo o un signo de dólar.
	- Los siguientes caracteres pueden ser números, guiones bajos o signos de dólar.
	- No esta permitido el uso de caracteres especiales o espacios.

#### Sensibilidad 
  JavaScript es Case Sensitive, es decir es sensible a mayúsculas y minúsculas. por ejemplo variable, Variable y VARIABLE son tres identificadores distintos.

#### Palabras Reservadas:
  También hay palabras reservadas que no se pueden usar como identificadores porque el lenguaje las reserva como por ejemplo, if, for, let, const, switch, etc.

#### Nomenclatura
	- Camel Case: Se suele usar para nombrar variables y funciones (miVar, sacarTotal).
	- Pascal Case: A menudo usado en clases (Producto, CocheElectrico).
	- Snake Case: No se suele usar en JS, pero usada a veces para constantes. (MAX_VALOR, URL_BASE).

#### Recomendaciones Identificadores
  Es recomendado usar nombres que describan para hacer el código más legible. (sumaTotal, nombreUsuario etc).

  Los identificadores largos no son una buena opción, JS no tiene un límite de longitud específico, pero es buna práctica mantenerlos de una longitud manejable.

### Sentencias:
  Una sentencia es la unidad mínima de ejecución. Es una instrucción que le dice al navegador que hacer. Cada sentencia puede llevar a cabo una acción, como declarar una variable, asignar un valor, ejecutar una función, controlar el flujo del programa mediante bucles y condicionales etc.

#### Estructura básica:
  Una sentencia puede ser tan simple como una variable o tan compleja como una serie de llamadas a funciones y operaciones.

#### Terminación:
  Por lo general las sentencias acaban en (;). Pero debido a la inserción Automático de punto y coma en JS, no siempre es necesario, aunque se recomienda ponerlos para evitar errores sutiles.

#### Ejemplos: 
  	- Declaración variables: let x = 5;
	- Asignación: x = 10;
	- Funciones: function miFuncion(){ … }
	- Condicionales: if(x>5){ … }
	- Bucles: for (let i = 0; i < 10; i++) { … }
	- Expresiones: console.log(x);

### Bloque:
  Un bloque de código es una sección de código fuente que esta delimitada por llaves {}. Estos bloques definen un ámbito o contexto en el cual se agrupan múltiples sentencias. Son fundamentales en la estructura y organización del código.

#### Agrupación:
  Permiten agrupar sentencias juntas para que puedan ser tratadas como una sola unidad. Esto es especialmente útil en estructuras de control de flujo como condicionales (if, else) y bucles (for, while). 

#### Ámbito de variables (Scope):
  Las variables declaradas dentro de un bloque de código son de ámbito local, esto significa que están accesibles solo dentro de ese bloque. Por ejemplo, una variable declarada dentro de un bloque if no es accesible fuera de ese bloque.

#### Estructuras de control:
  En estructuras de control de flujo, los bloques de código definen sentencias que se ejecutan en condiciones especificas. (como en if, else) o en cada iteración de un bucle (for, while).


### Comentarios:
	- Comentarios de una sola línea //
	- Comentarios de más de una línea o Comentarios de bloque. /**/

### Tipos de datos básicos:
	- String
	- Number
	- Boolean
	- Null
	- BigInt
	- Symbol

#### String: 
  Utilizado para representar datos textuales.
#### Number:
  Representa enteros y floats.
#### Boolean:
  Tiene dos valores true o false, es útil en operaciones lógicas y toma de decisiones en el flujo de control.
#### Undefined:
  Se utiliza para indicar una variable que ha sido declarada pero no se le ha asignado ningún valor.
   Puede ocurrir:
	- Cuando una variable es declarada pero no se le asigna un valor.
	- Al intentar acceder a una propiedad de un objeto que no existe.
	- Al intentar acceder a un elemento que no existe en un array.
	- Cuando una función no tiene una sentencia return explícita, devuelve undefined.
#### Null:
  Solo tiene un valor (Null), se utiliza para representar la ausencia intencional de un valor de objeto, en programación el valor Null hace referencia a una dirección invalida. Null significa que no hay valor porque se le ha indicado el programador.
#### BigInt:
  Este tipo permite trabajar con números enteros muy grandes, que superan el limite de los números de Number. Para usarlo hay que indicar al final del numero con una n.
#### Symbol:
  Las instancias de este tipo son únicas e inmutables, son útiles para crear identificadores únicos para propiedades de objetos.
  Ejemplo: let miSimbolo = Symbol('Mi identificador unico');

### ¿Qué tipo de dato tiene una variable?

#### typeof
  Es usado para determinar el tipo de una variable o expresión. Esto es útil en JS debido a su naturaleza de tipado dinámico, donde el tipo de una variable puede cambiar en tiempo de ejecución.
	- Sintaxis: typeof operando, donde operando es la variable o expresión cuyo tipo se quiere conocer.
	- Retorno: Devuelve una String que indica el tipo de la variable.
	- Valores de retorno: undefined, boolean, number, string, symbol, object o function.
#### Importancia typeof:
	- Declaración y validación: Permite a los programadores verificar el tipo de las variables durante la depuración y validar tipos de datos antes de realizar operaciones.
	- Evitar Errores: Al verificar el tipo de una variable antes de operar con ella, se pueden prevenir errores.

#### Limitaciones typeof:
	- No puede diferenciar entre un objeto y un array, o entre un objeto y null. Para estos casos, se suelen utilizar otros métodos como por ejemplo Array.isArray().
	. No se puede identificar tipos de objetos más específicos (como instancias de clases personalizadas). Para eso usaremos instanceof.

### Declaración e inicialización:
  Hay 3 maneras principales de declarar variables, cada una tiene sus características y niveles de alcance (Scope). 
	- Var (Variable de ámbito Global)
	- Let (Variable de ámbito local)
	- Const 

#### Var:
	- Tiene un alcance de función, es decir, esta disponible en toda la función en la que ha sido declarada, o globalmente si se declara fuera de una función.
	- Permite la Re declaración de la misma variable en el mismo ámbito.
	- Tiene lo que se conoce como "hoisting" (elevación), lo que significa que se puede usar la variable antes de su declaración en el código.

#### Let:
	- Permite declarar variables con alcance de bloque (block scope), lo que significa que la variable solo existe dentro del bloque en el que fue declarado.
	- No permite la re declaración de la misma variable dentro del mismo bloque.
	- Menos propenso a errores que var debido a su alcance de bloque y no permite el uso de la variable antes de su declaración.

#### Const:
	- Se utiliza para declarar constantes.
	- Tiene un alcance de bloque, similar a let.
	- No permite la re declaración ni la reasignación de la variable.
	- Debe ser inicializada en el momento de su declaración.
	- Aunque sea una variable declarada const es inmutable en términos de reasignación de su valor primitivo, si se trata de un objeto, las propiedades de ese objeto pueden ser modificadas.

#### var,let o const:
	- var se usa cada vez menos en el desarrollo moderno de JS, esto es debido a los problemas que puee causar.
	- let es preferible cuando se necesita una variable cuyo valor va a cambiar, como contadores en bucles, o valores que se reasignan en un bloque de código.
	- const es la mejor opción para declarar variables que no deben cambiar después de su asignación inicial. Esto mejora la legibilidad del código y redice la posibilidad de errores inesperados.
g