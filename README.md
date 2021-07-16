# Dog Lovers

![dog lovers](https://www.brandsmkt.com/wp-content/uploads/2020/06/dog-lover-760x506-1.jpg)

Despues de seguir este mini reto terminaras aprendiendo como trabajar de forma colaborativa con Github usando el [flujo de trabajo basadado en ramas por función (feature-branch workflow)](https://www.atlassian.com/es/git/tutorials/comparing-workflows/feature-branch-workflow), resolver los tan odiados conflictos como una pro y tambien aprenderemos los siguientes comandos de Git: 

### Basicos

- `git status`
- `git add`
- `git remote add`
- `git commit`
- `git push`  

### Colaborativos

- `git branch`
- `git checkout`
- `git pull`
- `git merge`

## Pasos 
### 1 - Nuestro primer PR

1. Dev2 hace fork del repo de colaboracion
2. Clonar el repo en el computador `git clone`
3. Establecer nuestras ramas remotas `origin` y `upstream`
4. Creamos nuestra primera branch `git branch mi-primera-tarea`
5. Cambiemos de branch `git checkout mi-primera-tarea`
6. Hagamos nuestro primer commit mostrando el flujo: `git status` -> `git add` -> `git commit`
7. Subimos nuestro avance a nuestra Github `git push origin mi-primera-tarea`
8. Hagamos nuestro primer Pull Request (PR) usando la plataforma de Github, colocamos un titulo y descripcion que comunique nuestra propuesta Por que?, que cambios aniade este PR?, subir imagenes o demos siempre ayuda
9.  Dev1 revisa que no haya conflictos, si todo esta bien aprobamos el PR, merge


### 2 - Sincronizando nuestro local con el remoto

1. Dev2 trae los cambios del repo principal (de integracion) `git pull origin master`
2. Creemos una nueva branch para cambiar los estilos de la app `git checkout -b trabajar-estilos` mientras que el Dev1 tambien crea una nueva branch para seguir trabajando en los estilos `git checkout -b aniadir-estilos`
3. Repetimos el flujo del paso 7-10 del primer acto


### 3 - Generamos un fucking conflicto

1. Dev1 sigue trabajando en su nueva branch `aniadir-estilos` y haciendo commits
2. Subir branch ha github `git push origin aniadir-estilos`
3. Realizamos un nuevo PR, 💣  conflictos!! 😨 
   
### 4 - Solucionando el fucking conflicto

1. Nos movemos hacia la rama master `git checkout master`
2. Nos sincronizamos con la rama remota master `git pull upstream master`
3. Nos movemos nuevamente a nuestra rama de trabajo `git checkout aniadir-estilos`
4. Mergeamos nuestra rama de trabajo con la rama master `git merge master`, 💣 aparecen los conflictos
5. Revisemos los conflictos a traves de la opcion del menu lateral "source control" que nos da VSCode
6. Con detenimiento tomamos las decisiones a cerca de que partes queremos mantener
7. Aniadimos los archivos con conflicto al stage `git add`
8. Realizamos un commit de la integracion
9. Actualizamos nuestro PR `git push origin aniadir-estilos`
10. Dev2 revisa que no haya conflictos, si todo esta bien aprobamos el PR, merge

## Resources

- [Flujo de trabajo de ramas de función en Git](https://www.atlassian.com/es/git/tutorials/comparing-workflows/feature-branch-workflow)