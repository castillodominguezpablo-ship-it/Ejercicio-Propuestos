# Ejercicio-Propuestos[ejercicios propuestos

● Un método que genere un diccionario de todos sus municipios y las
localidades que lo componen.
4.- Generar una comarca de prueba
Objetivos:
1. Crear una comarca con datos de prueba para verificar el funcionamiento de
las clases Localidad, Municipio y Comarca.
Requerimientos:
• Crear al menos dos municipios con varias localidades cada uno.
• Añadir estos municipios a la comarca.
• Mostrar la información de la comarca, incluyendo la población total y el
diccionario de municipios y localidades.
Pasos a seguir:
1. Crear localidades:
• Localidad 1:
• Nombre: Localidad1
• Población: 1000
• Municipio: Municipio1
• Localidad 2:
• Nombre: Localidad2
• Población: 2000
• Municipio: Municipio1
• Localidad 3:
• Nombre: Localidad3
• Población: 1500
• Municipio: Municipio2
• Localidad 4:
• Nombre: Localidad4
• Población: 2500
• Municipio: Municipio2
2. Crear municipios y añadir localidades:
• Municipio 1:
• Nombre: Municipio1
• Localidades:
• Localidad1
• Localidad2
• Municipio 2:
• Nombre: Municipio2
• Localidades:
• Localidad3
• Localidad4
3. Crear comarca y añadir municipios:
• Comarca:
• Nombre: Comarca de Prueba
• Municipios:
• Municipio1
• Municipio2
4. Mostrar información de la comarca:
• Nombre de la comarca: Comarca de Prueba
• Población total de la comarca: Suma de las poblaciones de todas las
localidades.
• Diccionario de municipios y localidades: Un diccionario donde las claves
son los nombres de los municipios y los valores son listas con los nombres
de las localidades que pertenecen a cada municipio.
Parte B
Crear un grafo ponderado no dirigido que permita representar la
conexión entre varias comarcas.
1.- Clase Grafo:
● Atributos:
○ nodos: colección de nodos, elija la representación de esta colección y
justifíquelo.
○ aristas: elija una representación para el conjunto de aristas del grafo y
justifique su elección.
● Constructor:
● Inicializa la lista nodos como vacía.
● Métodos:
○ agregarNodo(nodo): Añade un nodo al grafo.
○ eliminarNodo(nodo): Elimina el nodo
○ agregarArista(nodo1, nodo2, distancia): Añade una arista entre nodo1 y
nodo2 y asigna la distancia entre ellas. Si ya existe la arista actualiza su
distancia. Si no existe alguno de los nodos los agrega.
○ eliminarArista(nodo1,nodo2): elimina la arista que une nodo1 y nodo2. Si
no existe eleva una excepción.
○ distancia(nodo1, nodo2); devuelve la distancia entre los dos nodos en el
grafo. Si no están conectados devuelve None
○ comarcas_conectadas(nodo): devuelve un diccionario con las
comarcas que son vecinas del nodo dado como clave y la distancia
entre ellas como valor.
2. Código de prueba
Objetivos:
1. Crear un grafo de prueba con varias comarcas y conexiones entre ellas.
2. Mostrar la información del grafo, incluyendo las distancias entre comarcas y las
comarcas conectadas a una dada.
Pasos a seguir:
1. Crear el grafo:
• Crear un objeto de la clase Grafo.
2. Agregar nodos (comarcas):
• Añadir varios nodos representando comarcas al grafo.
3. Agregar aristas (conexiones entre comarcas):
• Añadir aristas entre los nodos con distancias específicas.
4. Mostrar información del grafo:
• Mostrar las distancias entre comarcas.
• Mostrar las comarcas conectadas a una dada.
Ejemplo de implementación:
# Crear el grafo
grafo = Grafo()
# Agregar nodos
grafo.agregarNodo("Comarca1")
grafo.agregarNodo("Comarca2")
grafo.agregarNodo("Comarca3")
grafo.agregarNodo("Comarca4")
# Agregar aristas
grafo.agregarArista("Comarca1", "Comarca2", 10)
grafo.agregarArista("Comarca1", "Comarca3", 15)
grafo.agregarArista("Comarca2", "Comarca4", 20)
grafo.agregarArista("Comarca3", "Comarca4", 25)
# Mostrar información del grafo
print(f"Distancia entre Comarca1 y Comarca2: {grafo.distancia("Comarca1",
"Comarca2")}")
print(f"Comarcas conectadas a Comarca1:
{grafo.comarcas_conectadas("Comarca1")}")
3. Función para encontrar el centro del grafo
Objetivos:
1. Escribir una función que devuelva el centro del grafo, es decir, el nodo con la
menor distancia máxima a todos los demás nodos.
Pasos a seguir:
1. Calcular las distancias máximas:
• Para cada nodo, calcular la distancia máxima a todos los demás nodos.
2. Encontrar el nodo con la menor distancia máxima:
• Comparar las distancias máximas y encontrar el nodo con la menor
distancia máxima.
Parte C
Crear índices de localidades mediante un árbol ordenado.
Se harán índices por nombre y por población. Se realizarán consultas buscando en el
índice y filtrados según diferentes predicados, que se pasarán como parámetro como
expresiones lambda.
1. Clase ÁrbolOrdenado:
• Atributos:
• raíz: nodo raíz del árbol.
• Constructor:
• Inicializa el árbol como vacío.
• Métodos:
• insertar(valor, mayor): Inserta un valor en el árbol. La función mayor
es el comparador para la ordenación de los nodos en el árbol.
• buscar(valor): Busca un valor en el árbol y devuelve el nodo
correspondiente.
• filtrar(predicado): Devuelve una lista de valores que cumplen con
el predicado dado.
• recorrido_ordenado(): Devuelve una lista de valores en el árbol en
orden ascendente.
2. Funciones para manejar índices de localidades:
• generar_arbol_por_nombre(localidades): Genera un árbol ordenado por
nombre a partir de una lista de localidades.
• generar_arbol_por_poblacion(localidades): Genera un árbol ordenado
por población a partir de una lista de localidades.
• mostrar_arbol_en_orden(arbol): Muestra el árbol en un recorrido
ordenado.
• buscar_en_arbol(arbol, valor): Busca un valor en el árbol.
• filtrar_en_arbol(arbol, predicado): Filtra los valores en el árbol según un
predicado dado.
3. Código de prueba:
• Crear árboles de prueba con datos de localidades.
• Realizar consultas y filtrados en los árboles por nombre y por población.
