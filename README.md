DIY BookClub (DIYBookClub_Starter)

Documentación Técnica del Proyecto — MIT App Inventor 2


Autora: Brenda Arana Gutiérrez

1. Descripción General del Proyecto
DIY BookClub es una aplicación móvil desarrollada en MIT App Inventor 2 que permite a los
usuarios compartir y explorar reseñas de libros en tiempo real. La plataforma habilita la lectura
de opiniones, la publicación de nuevas reseñas de libros (título y contenido) y el
almacenamiento persistente mediante CloudDB.

2. Estructura de Pantallas e Interfaz de Usuario
Screen1 (Publicación y Navegación Principal):
 Modo Escribir Reseña (EscribirReseña): Contiene los campos de texto TitleTextBox
(Título del libro) y TextBox2 (Reseña del libro) junto con el botón PublicarButton.
 Modo Leer Reseña (LeerReseña): Permite alternar visualmente hacia el contenedor de
lectura de libros.
 Botón Libros: Redirige a la pantalla Screen2 mediante la función de apertura de pantallas.
Screen2 (Catálogo y Detalle de Libros):
 ListView1 / ViewLista1: Componente de lista para mostrar todos los títulos guardados en
la base de datos.
 CloudDB1: Componente de almacenamiento distribuido para sincronizar títulos y reseñas.
 BotonVolver: Regresa a la pantalla principal Screen1.

3. Arquitectura del Flujo de Datos
[Título + Reseña] ➔ PublicarButton ➔ CloudDB1.AppendValueToList ➔ [Screen2: ListView1] ➔ Selección ➔ Ver Reseña Completa
