1) Aplicación del encapsulamiento

Todos los atributos de las clases (Materia, Estudiante y Carrera) fueron declarados como privados, garantizando que no puedan ser accedidos directamente desde fuera de la clase.
El acceso a dichos atributos se controla a través de métodos getters y setters, lo que asegura la protección y consistencia de los datos.
Ejemplo: en Materia, atributos como nombre, codigo, creditos y calificacion solo pueden ser modificados mediante sus setters, que imponen restricciones de validez.


2) Implementación de relaciones entre clases

Composición:
Estudiante contiene una lista de Materia (ArrayList<Materia>). Esto significa que un estudiante está compuesto por varias materias.
Carrera contiene una lista de Estudiante (ArrayList<Estudiante>), indicando que una carrera está compuesta por múltiples estudiantes.

Asociación:
En el main de App, se crean instancias de Carrera, Estudiante y Materia que luego son asociadas mediante métodos como agregarMateria() o agregarEstudiante().
Con estas relaciones se refleja un modelo académico realista: una carrera tiene estudiantes y cada estudiante cursa distintas materias.


3) Validaciones en los métodos setter

En Materia:
setNombre() y setCodigo(): validan que no se asignen valores null ni cadenas vacías.
setCreditos(): asegura que los créditos sean mayores a cero.
setCalificacion(): solo admite calificaciones entre 0 y 10.
En Estudiante:
setNombre() y setApellido(): validan que no se ingresen valores nulos ni vacíos.
setEdad(): solo permite asignar edades mayores a 16 años, reflejando una restricción lógica en el dominio del problema.