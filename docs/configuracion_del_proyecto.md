# Configuración del Proyecto 🚀

El proyecto hace uso de tres herramientas clave: 

- [Devcontainers](https://code.visualstudio.com/docs/remote/containers)
- [Poetry](https://python-poetry.org/)
- [MkDocs](https://www.mkdocs.org/)
  
 EL objetivo es asegurar que todos los desarrolladores trabajen en un entorno consistente y controlado, y que la documentación sea accesible y fácil de mantener. Creo firmemente que el uso de estas herramientas puede ser especialmente útil en un entorno de colaboración como el de Keepler, donde varios ingenieros pueden trabajar en un mismo proyecto. Además, facilitan la transición hacia la producción al garantizar que el código se ejecutará en un entorno con las mismas dependencias que se especificaron durante el desarrollo, y que la documentación se mantendrá actualizada.

## Devcontainers 📦

Los Devcontainers nos permiten definir un entorno de desarrollo que se ejecuta dentro de un contenedor Docker. Esto nos proporciona un entorno consistente y reproducible, lo que facilita el trabajo en equipo y evita el famoso "en mi máquina sí funciona". Además, asegura que cualquier prueba o implementación en producción se haga en un entorno idéntico al de desarrollo, lo que aumenta la confiabilidad del software.

Para usar Devcontainers, necesitas:

1. [Docker](https://www.docker.com/products/docker-desktop) instalado en tu máquina.
   
2. [Visual Studio Code](https://code.visualstudio.com/download) como tu editor de código.
   
3. La extensión [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) instalada en VS Code.

Una vez que tienes todo esto, simplemente abre este proyecto en VS Code, y te pedirá automáticamente que abras el proyecto en un contenedor. Acepta, y ¡listo! Ya tienes tu entorno de desarrollo configurado y listo para usar.

## Poetry 📚

Poetry es una herramienta para la gestión de dependencias en Python. Nos permite definir las bibliotecas de las que depende nuestro proyecto y garantizar que todos estemos utilizando las mismas versiones. Esto es vital en un entorno colaborativo para evitar conflictos de versiones y asegurar la coherencia en todo el proyecto. Además, Poetry simplifica el proceso de empaquetado y publicación del software, lo que facilita la transición a la producción.

Dentro del Devcontainer, nuestro proyecto ya tiene Poetry preinstalado. Para instalar las dependencias de nuestro proyecto, simplemente abre una terminal en VS Code (que ahora se ejecutará dentro del Devcontainer) y ejecuta:

    poetry install

Esto instalará todas las dependencias necesarias para nuestro proyecto. Para agregar una nueva dependencia, puedes usar el comando `poetry add`. Por ejemplo:

    poetry add numpy

Esto es similar a usar `pip install numpy`, pero con la ventaja de que Poetry automáticamente actualizará tu archivo `pyproject.toml` para reflejar la nueva dependencia.

Poetry también ofrece una serie de comandos útiles, como `poetry show --tree` que muestra las dependencias de tu proyecto en un formato de árbol.

## MkDocs 📖

MkDocs es una herramienta rápida y simple para crear sitios web de documentación a partir de archivos de Markdown. Se utiliza en este proyecto para asegurar que la documentación sea fácilmente accesible y esté bien estructurada. Esto es particularmente útil en un entorno de colaboración y producción, ya que permite a todos los miembros del equipo, así como a los stakeholders, tener un fácil acceso a la documentación actualizada del proyecto.

¡Y eso es todo! Con estos pasos, ya tienes tu entorno de desarrollo configurado y listo para usar. Estas herramientas son esenciales para el desarrollo de software moderno, y estoy seguro de que aportarán valor a Keepler. 🤗
