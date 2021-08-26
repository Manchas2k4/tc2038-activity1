![Tec de Monterrey](images/logotecmty.png)
# Actividad integradora 1

## <span style="color: rgb(26, 99, 169);">¿Qué tengo que hacer?</span>
Accede a la siguiente liga: [Act. 0](https://classroom.github.com/a/458xemuA) y acepta la tarea. Esto creará tu repositorio de trabajo. En él, encontrarás el archivo "main.cpp". En este archivo deberás desarrollar la implementación del problema presentado en esta actividad.  En la parte superior del archivo coloca, en comentarios, tus datos. Por ejemplo:
```
// =========================================================
// File: main.cpp
// Author: Edward Elric - A00123456
// Date: 01/01/2021
// =========================================================
```
Implementa, <span style="text-decoration-line: underline;">forma individual</span>, un programa que lea 5 archivos de texto:
- transmission1.text
- transmission2.text
- mcode1.text
- mcode2.text
- mcode3.text

Todos los archivo contiene exclusivamente carácteres del 0 al 9 y de la A a la F.

Los archivos de transmisión (transmission1.txt, transmission2.txt) contienen carácteres de texto que representan los datos envíados de un dispositivo a otro. Mientras que los archivos mcode1.txt, mcode2.txt y mcode3.txt contienen el código malicioso que buscaremos dentro de las transmisiones.

### Parte 1
Tu solución debe determinar si existen algunos de los códigos maliciosos en ambos archivos de transmisión. En caso de que se encuentre alguno de los códigos maliciosos, se desplegrará *true*, seguido de la posición en el archivo de transmisión donde inicia ese código malicioso. Por ejemplo:
```
transmission1.txt:
code1.txt - true, start at position 10
code2.txt - false
code3.txt - true, start at position 789

transmission2.txt:
code1.txt - true, start at position 8
code2.txt - true, start at position 402
code3.txt - true, start at position 2508
```
### Parte 2
Tu solución también debe considerar que pueden existe códigos maliciosos desconocidos que debemos buscar. Para simplificar nuestro trabajo y como una forma de diversión, los "amables" piratas informáticos han colocados estos códigos maliciosos nuevos en formato "espejeado" (o palídromos). Si tu solución encuentra un código malicioso de este estilo, debera desplegar en una sola línea en que posición inicia y termina el código "espejeado" más largo que ha encontrado. Puedes asumir que siempre encontrarás este tipo de código. Por ejemplo:
```
transmission1.txt:
mirrored code found, start at 35, ended at 130

transmission2.txt:
mirrored code found, start at 577, ended at 1765
```
### Parte 3
Finalmente, tu solución dede terminar que tan similares son los archivos de transmisión, desplegando la posición de inicio y fin en el primer archivo donde se encuentra la subcadena común más larga. Por ejemplo:
```
the longest common substring starts at position 141 and ends at 399 in the transmission1.txt file
```

## <span style="color: rgb(26, 99, 169);">**Entrada**</span>
Ninguna, solamente debe procesar los archivos mencionados al inicio del problema.

## <span style="color: rgb(26, 99, 169);">**Salida**</span>
Deberá desplegar los resultados de cada uno de los análisis, separados por un salto de línea.

## <span style="color: rgb(26, 99, 169);">**Ejemplo de salida**</span>
```
transmission1:
code1.txt - true, start at position 10
code2.txt - false
code3.txt - true, start at position 789

transmission2:
code1.txt - true, start at position 8
code2.txt - true, start at position 402
code3.txt - true, start at position 2508

transmission1:
mirrored code found, start at 35, ended at 130

transmission2:
mirrored code found, start at 577, ended at 1765

the longest common substring between transmission1.txt and transmission2.txt is 517 characters long
```

<br>Todas las funcionalidades deberán de estar correctamente alineadas y documentadas.&nbsp; Recuerda que todas las funcionalidades deberán pasar exitosamente todas las pruebas. Como parte de la documentación deberá incluirse la complejidad de cada una de ellas.

Para probar tu implementación, compila tu programa con el comando:
```
g++ -std=c++11 main.cpp -o app
```
Posteriormente, ejecuta tu programa. Para realizar las pruebas, puedes usar las siguientes líneas de código.
```
./app > mysolution.txt
diff mysolution.txt solution.txt
```
Si el segundo comando no tiene ninguna salida, los resultados que obtuviste son los esperados.

## <span style="color: rgb(26, 99, 169);">**¿Bajo qué criterios se evalúa mi evidencia?**</span>

- **85%** - Genera la salida esperada.
- **15%** - El código deberá seguir los lineamientos estipulados en el estándar de codificación: <span class="instructure_file_holder link_holder">[liga_estándar_codificación](estandar.pdf)</span>

## <span style="color: rgb(26, 99, 169);">**¿Dónde la entrego?**</span>
Cuando hayas pasado todas las pruebas, recuerda publicar el código en tu repositorio (*git push*).
