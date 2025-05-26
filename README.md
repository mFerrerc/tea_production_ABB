# Sistema Automatizado de Empaquetado de Té

Este repositorio contiene el desarrollo completo de un proyecto de automatización llevado a cabo en el Grado en Ingeniería Robótica. El objetivo ha sido diseñar, simular y documentar una estación automatizada capaz de empaquetar bolsas de té en cajas, de forma completamente autónoma, utilizando robots industriales y cintas transportadoras.
c![image](https://github.com/user-attachments/assets/8d74865f-e777-4591-8e08-cd07c62a1524)

## Descripción general del proyecto

El sistema simula una línea de empaquetado en la que intervienen tres robots industriales ABB IRB 365 y cuatro cintas transportadoras. Los robots realizan tareas de alimentación, colocación y cierre de cajas, mientras que las cintas se encargan del transporte de bolsas, cajas y tapaderas en distintas fases del proceso.
![image](https://github.com/user-attachments/assets/900224fe-4e8a-4ba5-ad4e-626431681718)

Todo el sistema ha sido diseñado y probado en el entorno de simulación RobotStudio, y ha sido programado en lenguaje RAPID, el estándar de ABB para robots industriales. Además, los objetos utilizados, como las cajas, bolsas, tapaderas y herramientas de sujeción, han sido diseñados en Autodesk Inventor y posteriormente integrados en la simulación.
![image](https://github.com/user-attachments/assets/cd4cdc36-e847-4410-8748-5e6a9cd9a0b1)

## Estructura y funcionamiento

El flujo de trabajo se inicia con la generación de una caja vacía, que es transportada a la estación de llenado. Mientras tanto, los robots 1 y 2 colocan bolsas de té sobre una cinta, que las conduce hasta el robot 3. Este robot recoge las bolsas y las coloca cuidadosamente dentro de la caja, formando dos capas de 12 unidades cada una. Una vez llena, el robot recoge una tapadera de otra cinta y la coloca sobre la caja. Finalmente, la caja cerrada es empujada por un pistón hacia una cuarta cinta que la saca del sistema.
![image](https://github.com/user-attachments/assets/e18af599-37c3-4a3d-b5f4-6b3c327cdba9)

Todo el proceso está gestionado mediante sensores y señales digitales que aseguran una sincronización precisa entre robots y estaciones. Se ha prestado especial atención a la lógica de control, dividiendo cada parte del sistema en ciclos claros y bien definidos.

## Elementos destacados

Uno de los elementos clave del proyecto es el diseño del efector final de doble ventosa utilizado por los robots. Esta herramienta permite una manipulación rápida y segura de bolsas y tapaderas, y cuenta con sensores que verifican si el agarre ha sido exitoso antes de continuar con la operación.

Otro aspecto fundamental ha sido la programación distribuida entre los distintos controladores, permitiendo una cooperación fluida entre los tres robots. La coordinación de las cintas transportadoras mediante sensores intermedios y señales digitales también ha sido determinante para asegurar la eficiencia del ciclo completo.

## Resultados y simulación

El sistema logra empaquetar una caja completa (24 bolsas) en menos de un minuto, cumpliendo así con el objetivo de rendimiento propuesto. Se han realizado dos simulaciones: una de ciclo único (empaquetado de una sola caja) y otra de ciclo continuo (cadena sin fin), esta última con un comportamiento más complejo debido a la necesidad de mantener múltiples procesos activos de forma simultánea.

El vídeo de la simulación puede consultarse en el siguiente enlace:

[▶️ Ver vídeo de la estación funcionando](https://youtu.be/tINdL7jqoJw)

## Cómo ejecutar la simulación

Para reproducir el entorno en RobotStudio, es necesario instalar la versión RobotWare 7.18.1. Se deben reiniciar los controladores de los tres robots, restablecer el estado inicial del entorno y ejecutar el ciclo. En ocasiones es recomendable repetir el procedimiento una segunda vez tras abrir el proyecto, para asegurar que todas las señales se inicializan correctamente.

---

Este proyecto refleja una aproximación realista a un proceso industrial de empaquetado, y constituye una base sólida para su posible adaptación a aplicaciones reales. Combina diseño mecánico, programación de robots, lógica de control y simulación industrial, demostrando la importancia de la sincronización y la fiabilidad en entornos automatizados.

