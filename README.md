# Examen_Biblioteca_Municipal_3_trimestre

## Enunciado
Se desea modelar el funcionamiento de una biblioteca municipal, teniendo en cuanta que:

Los libros se organizan según la temática. Sabemos que cada temática se encuentra alojada en una planta de la biblioteca. Además, se deben registrar los libros que se encuentran en la biblioteca. Cada libro contará con un identificador, titulo, autor, editorial; por cada libro puede haber más de un ejmplar disponible para el préstamo. Por cada préstamo deberá almacenarse el ejemplar, la fecha de préstamo, la fecha de entrega estimada y la real. El préstamo máximo será de 30 días. Los lectores que no entreguen el libro a tiempo tendrán penalización. Para aplicar esa penalización, la biblioteca cuenta con una ficha por cada lecotr, con su número de identificación o pasaporte, su nombre, y su dirección postal. Para fomentar la lectura, los emploados de la biblioteca, que poseen su propia identificación como tales, pueden llevar libros a casa por un plazo mayor que los usuarios convencionales. También es importante que el préstamo del libro se realiza mediante un bibliotecario.

En todo momento, debes indicar getters, setters y no es recomendable dejar ninguna clase sin métodos.

Crea el diagrama de clases correspondiente.

## Mi solución

![image](https://github.com/ToniRiutort/Examen_Biblioteca_Municipal_3_trimestre/assets/104781981/0cce65d5-3e9c-45d5-ae68-550dc435cec8)

Al leer el enunciado lo primero que he hecho ha sido identificar las diferentes clases del diagrama de clases, que han sido:

- Libros

- Planta

- Préstamo

- Lector

- Bibliotecario

Luego al empezar a plantearme cómo hacer el diagrama me he dado cuenta de que necesitaba la clase abstracta biblioteca, sobre la clase planta y libros, y además necesitaba una clase abstracta persona, sobre la clase lector y bibliotecario. 

Después de definir bien las clases lo siguiente ha sido identificar los atributos de cada clase.

Lo siguiente ha sido pensar las relaciones entre las clases, en mi caso he pensado en que la clase lector hereda todo de la clase persona, que a su vez bibliotecario hereda de lector, lo planteo así ya que el bibliotecario no deja de ser lector al ser bibliotecario, al contrario tiene más privilegios sobre el lector a la hora de tomar prestados libros. Además la clase bibliotecario está relacionada con la clase biblioteca, que es una relación de composición donde la clase biblioteca es la clase fuerte, ya que sin biblioteca no hay bibliotecarios.

![image](https://github.com/ToniRiutort/Examen_Biblioteca_Municipal_3_trimestre/assets/104781981/afea0726-6447-46e6-b8b8-393d76ba98b6)

La clase planta está relacionada con una relación de composición con la clase biblioteca, donde la fuerte es biblioteca, ya que sin biblioteca no habría plantas, además la clase planta está relacionada con una relación de composición con la clase libros, donde la fuerte es libros ya que sin libros de una temática no es necesaria una planta sobre esa temática.

![image](https://github.com/ToniRiutort/Examen_Biblioteca_Municipal_3_trimestre/assets/104781981/36ac2a8f-8ae6-4e81-af84-e9a094e1ff47)

Por último tenemos la clase préstamo que está relacionada con la clase libro, la clase lector y la clase bibliotecario. La relación con la clase libros es una relación de composición, donde la fuerte es la clase libro, ya que sin libros no hay préstamos. La relación con la clase lector es una relación de composición, ya que si no hay lector que quiera un libro no puede haber préstamos de libros. Por último, la relación con la clase bibliotecario es una relación de composición, donde la fuerte es bibliotecario, ya que si no hay un bibliotecario no se puede hacer un préstamo, ya que el préstamo se tiene que hacer a través de un bibliotecario. 

![image](https://github.com/ToniRiutort/Examen_Biblioteca_Municipal_3_trimestre/assets/104781981/aaef2e42-387f-4e3e-bc75-af2300735581)
