# EN CONSTRUCCION
# VERSIO ALFA 1

# granja_minera_monero_raspberry
Proyecto experimental y educativo para el despliege automatizado de nodos servidores con Ansible. tomando como ejemplo, el despliege de nodos mineros en placas Raspberry 2 y 3.

El presente proyecto, se basa en el repositorio "https://github.com/lucasjones/cpuminer-multi.git" alojado en Github por el usuario "lucasjones".
Este proyecto, es uno de los aconsejados por la página https://minergate.com/ como minero de terminal utilizando la CPU como recurso minero.
El minero se ejecutará para minar la criptomoneda "monero" con sus siglas "XMR". Si se desea minar otra moneda, se puede consutar en el repositorio indicado de "lucasjones".

Requisitos:
0.- crear una cuenta en el portal "https://minergate.com". Es gratuita y simplemente necesitas tener una cuenta de correo.
1.- tener instalado Ansible. Si no conoces que es Ansible, lo primero que tendrias que hacer es documentarte en su página oficial. como introducción. se trata de una erramienta de orquestación de sistemas.
2.- Tener instalado el servicio ssh en los nodos destinos. en este caso utilizamos la distribución oficial "Raspbian Stretch Lite" se que puede bajar de su página oficial https://www.raspberrypi.org/downloads/raspbian/.
3.- configurar ssh en los nodos destino que se añaden al inventario "mineros" para que permita acceso ssh como "root" y ejecutar las orden emitidas por Ansible.
4.- genetar "key ssh" en equipo que corre "ansible"
5.- copiar "key publica ssh" al usuario "root" de los nodos
6.- configurar variables con los datos de la cuenta de correo creada en el paso "0"
7.- Lanzar "ansible-playbook -i mineros mineros.yml

NOTA: Si se quiere desde el propio nodo, lanzar el minero, se ha desplegado el scrip "/home/pi/minergate/minar.sh" que solicitará por terminal los mismos datos que se introducen con variables desde Ansible, pero en este caso, es el usuario el que interactua con el terminal e introduce los datos.
