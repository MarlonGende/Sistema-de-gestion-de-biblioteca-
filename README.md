# Sistema de gestión de biblioteca

## Descripción

El sistema será una aplicación de escritorio o web destinada al uso de los 
bibliotecarios y asistentes. 
Los usuarios podrán registrar nuevos libros, consultar su disponibilidad, registrar 
préstamos y devoluciones, y obtener listados básicos de información. 

## Objetivos

El propósito del sistema es facilitar la administración de los libros y préstamos en una 
pequeña biblioteca. 
Permitirá registrar libros, gestionar usuarios y controlar los préstamos y devoluciones. 

## Requerimientos

### Funcionales

Requerimientos | Descripción | Tipo 
-------:|:-------------:|:------------
RF1  | El sistema debe permitir registrar nuevos libros con título autor, año y código único. | Entrada
RF2 | El sistema debe permitir buscar libros por título o autor. | Consulta
RF3 | El sistema debe enviar un recordatorio por correo a los usuarios con préstamos vencidos. | Proceso 
RF4 | El sistema debe permitir registrar la devolución de un libro prestado. | Actualización
RF5 | El sistema debe mostrar el estado del libro (disponible o prestado). |   Salida

### No Funcionales

Requerimientos | Descripción | Tipo 
-------:|:-------------:|:------------
RNF1 | Las búsquedas deben ejecutarse en menos de 3 segundos. | Rendimiento
RNF2 | Solo usuarios con rol de administrador Rendimiento pueden eliminar registros. | Seguridad
RNF3 | La interfaz debe ser fácil de usar y mostrar mensajes claros al usuario. | Usabilidad

## Pruebas

### Unitaria

Pruebas (PU)  | Requerimiento Asociado | Datos de Entrada | Resultado Esperado | Resultado Obtenido (Simulado)
-------:|:------:|:---:|:----:|:------------
PU1 | RF1 | Libro: “El Quijote”, Autor: “Cervantes”, Año: 1605, Código: Q001 |  El libro se registra correctamente. |Correcto
PU2 | RF2| Búsqueda: Por autor:  “Cervantes” Por título: “El Quijote” | Muestra todos los libros de Cervantes o el libro que se buscó por el titulo | Correcto
PU3 | RF3 | Usuario(correo) Con préstamo vencido | Se envía correo de recordatorio | Correcto

### Validación

Pruebas (PV)  | Requerimiento Asociado | Datos de Entrada | Resultado Esperado | Resultado Obtenido (Simulado)
-------:|:------:|:---:|:----:|:------------
PV1 | RNF1 | Busca “Cervantes” Se tienen 300 libros registrados | Resultados en menos de 3 segundos. | Correcto
PV2 | RNF3 | Usuario nuevo utiliza el sistema sin ayuda | Puede registrar, buscar y prestar libros sin errores | Correcto

## Tipo de mantenimiento propuesto 

Los mantenimientos que se sugieren son: 
- Preventivo
- Perfectivo

## Reflexión

- Las pruebas permiten verificar que cada requerimiento se cumple en la práctica, no solo 
en la teoría. 
- Las pruebas unitarias aseguran que cada función del sistema como registrar libros o 
enviar recordatorios funcione correctamente de manera independiente. 
- Mientras tanto, las pruebas de validación comprueban que el sistema responde 
adecuadamente en condiciones reales de uso. 
