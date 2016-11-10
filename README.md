# laboratorio-practico


## 1)	Investigar.
a.	 ¿Qué es Git?, ¿Que lo hace diferente a otros sistemas de versionamiento?
b.	¿Qué es Github?, ¿Por qué es importante para nosotros en este curso?
Explicar los siguientes comandos en sus propias palabras. 
git clone: obtener una copia de un repositorio Git existente
Puedes clonar un repositorio con git clone [url]. Por ejemplo, si quieres clonar la librería Ruby llamada Grit, harías algo así:
$ git clone git://github.com/schacon/grit.git
git pull: Incorpora cambios con respecto a un repositorio remoto en la rama actual.

git pull [opciones] [<repositorio> [<refspec> ...]]

<repositorio> debe ser el nombre de un repositorio remoto como los pasados a git-fetch [1] . <Refspec> puede nombrar a un árbitro a distancia arbitraria (por ejemplo, el nombre de una etiqueta) o incluso una colección de referencias con ramas de seguimiento remoto correspondiente (por ejemplo, refs / heads / *: refs / mandos a distancia / origen / *), pero por lo general, es el nombre de una rama en el repositorio remoto.

Los valores por defecto para <repositorio> y <branch> se lee de la "distancia" y "fusionar" la configuración de la rama actual según lo establecido por git-rama [1] --track .


OPCIONES

-q
--tranquilo

    Esto se pasa al tanto que subyace git-fetch para aplastar a la presentación de informes de durante el traslado y subyacente git-fusión para aplastar salida durante la fusión. 
-v
--verboso
    Pase al --verbose git-fetch y git-fusión. 
- [No-] recurse-submódulos [= yes | On-Demand | no]

Opciones relacionadas con la fusión 
--cometer 
--no-commit 
Realizar la combinación y comprometer el resultado. Esta opción se puede utilizar para anular --no-commit. 
Con --no-commit realizar la combinación, pero pretender que la fusión fallida y no confirmación automática, para dar al usuario la oportunidad de inspeccionar y modificar el resultado de la fusión antes de comprometerse aún más. 
--editar 
-mi 
--sin editar 
Invocar un editor antes de comprometer el éxito de combinación mecánica para modificar aún más el mensaje de mezcla generada automáticamente, de modo que el usuario puede explicar y justificar la fusión. El --no-edit opción se puede utilizar para aceptar el mensaje de auto-generado (esto se suele desalentar). 
guiones de edad avanzada pueden depender del comportamiento histórico de no permitir al usuario editar el mensaje de registro de fusión. Ellos verán un editor abierto cuando se ejecutan git merge . Para que sea más fácil para ajustar dichas secuencias de comandos para el comportamiento actualizado, la variable de entorno GIT_MERGE_AUTOEDIT se puede configurar para no al comienzo de ellos. 
--ff 
Cuando la fusión se resuelve como un avance rápido, sólo se actualizará el puntero rama, sin crear una fusión cometió. Este es el comportamiento predeterminado. 
--no-ff 
Crear una combinación de cometer incluso cuando la fusión se resuelve como un avance rápido. Este es el comportamiento por defecto cuando la fusión de una anotada (y posiblemente firmado) etiqueta. 
--ff de sólo 
Negarse a fusionar y salida con un estado distinto de cero a menos que el actual HEAD es ya hasta a la fecha o la combinación puede ser resuelto como un avance rápido. 
--log [= <n>] 
--no-log 
Además de los nombres de rama, poblar el mensaje de registro con las descripciones de una línea de en la mayoría de <n> commit reales que se están fusionadas. Ver también git-fmt-merge-msg [1] . 
Con --no-log no anotar las descripciones de una sola línea de las confirmaciones reales se fusione. 
--stat 
-norte 
--no-stat 
Mostrar una diffstat al final de la fusión. El diffstat también es controlado por la opción de configuración merge.stat. 
Con -n o --no-stat no muestran una diffstat al final de la fusión. 
--squash 
--no-calabaza 
Producir el estado del árbol y el índice de trabajo como si una verdadera fusión ocurrió (a excepción de la información de combinación), pero en realidad no hacen un commit, mover la HEAD , o registro $GIT_DIR/MERGE_HEAD (para hacer que el próximo git commit comando para crear una fusionar comprometerse). Esto le permite crear una única confirmación en la parte superior de la rama actual, cuyo efecto es el mismo que la fusión de otra rama (o más en caso de un pulpo). 
Con --no-calabaza realizar la combinación y comprometer el resultado. Esta opción se puede utilizar para anular --squash. 
-s <estrategia> 
--strategy = <estrategia> 
Utilizar la estrategia de combinación dada; se pueden suministrar más de una vez para especificar en el orden en que deben ser juzgados. Si no hay -s opción, una lista integrada de las estrategias se utiliza en su lugar (git merge-recursiva cuando la fusión de una sola cabeza, git merge-pulpo de otro modo). 
-X <Opción> 
-Opción --strategy = <opción> 
Pasar opción específica estrategia de combinación a través de la estrategia de combinación. 
--verify firmas 
-firmas --no-verificar 
Verificar que la punta de cometer la rama lateral está fusionando está firmado con una clave válida, es decir, una llave que tiene un fluido válida: en el modelo de confianza predeterminado, esto significa que la clave de firma ha sido firmada por una clave de confianza. Si la punta de cometer la rama lateral no está firmado con una clave válida, la fusión se aborta. 
--resumen 
--no-Resumen 
Los sinónimos para --stat y --no-stat; éstos están en desuso y se eliminará en el futuro. 
--allow-no relacionadas-historias 
De forma predeterminada, git merge comando se niega a fusionar historias que no comparten un ancestro común. Esta opción se puede utilizar para anular esta seguridad al combinar las historias de dos proyectos que comenzaron su vida de forma independiente. Ya que es una ocasión muy rara, hay una variable de configuración para habilitar esto por defecto existe y no se añadirá. 
-r 
--rebase [= false | true | preservar | interactiva] 
Cuando es verdadero, rebase la rama actual en la parte superior de la rama ascendente después de obtenerlo. Si hay una rama de seguimiento a distancia correspondiente a la rama aguas arriba y aguas arriba de la rama se reajusta desde el pasado captada, el rebase utiliza esa información para evitar un rebase cambios no locales. 
Cuando se ajusta a preservar, rebase con el --preserve-merges opciones transferida a git rebase de manera que la fusión creada localmente comete no se aplana. 
Opciones relacionadas con ir a buscar 
--todas 
Fetch todos los controles remotos. 
-un 
--adjuntar 
Anexar al árbitro nombres y nombres de objeto de árbitros captadas que el contenido existente de .git/FETCH_HEAD . Sin esta opción, los datos antiguos en .git/FETCH_HEAD será sobrescrita. 
--depth = <profundidad> 
Limitar ir a buscar al número especificado de confirmaciones de la punta de cada rama de la historia remota. Si ir a buscar a un depósito superficial creada por git clone con --depth=<depth> opción (véase git-clone [1] ), profundizar o acortar la historia al número especificado de confirmaciones. Etiquetas para las confirmaciones profundizadas no se obtendrán. 
--unshallow 
Si el repositorio de código fuente es completa, convertir un depósito superficial para una completa, la eliminación de todas las limitaciones impuestas por los depósitos someros. 
Si el repositorio de código fuente es poco profunda, se ha podido recuperar tanto como sea posible para que el repositorio actual tiene la misma historia como el repositorio de origen. 
--update poco profunda 
Por defecto se deben recuperar desde un repositorio de poca profundidad, git fetch se niega referencias que se tienen que actualizar .git / superficial. Esta opción actualiza .git / superficial y aceptan tales referencias. 
-F 
--fuerza 
Cuando se utiliza git fetch con <rbranch>:<lbranch> refspec, se niega a actualizar la rama local <lbranch> menos que el grupo control remoto <rbranch> se obtiene es un descendiente de <lbranch> . Esta opción anula el registro de entrada. 
-k 
--guardar 
Mantenga el paquete descargado. 
--no-etiquetas 
Por defecto, las etiquetas que apuntan a objetos que se descargan desde el repositorio remoto se recuperan y se almacenan localmente. Esta opción se desactiva esta siguiente automática de etiquetas. El comportamiento predeterminado de un control remoto puede ser especificado con el mando a distancia. <Nombre> configuración .tagOpt. Ver git-config [1] . 
-u 
--update-cabeza-ok 
Por git por defecto se ha podido recuperar niega a actualizar la cabeza que corresponde a la rama actual. Esta opción deshabilita el registro de entrada. Esto es puramente para el uso interno de git pull para comunicarse con git fetch, y, a menos que esté implementando su propia porcelana no se supone para usarlo. 
--upload-pack <carga-pack> 
Cuando se le presente, y el repositorio para ir a buscar a partir es manejado por git fetch-Pack, --exec=<upload-pack> se pasa al comando para especificar la ruta no predeterminada para el comando de marcha en el otro extremo. 
--Progreso 
estado de progreso se informó sobre la secuencia de error estándar de forma predeterminada cuando está conectado a un terminal, a menos que se especifique -q. Este estado fuerzas bandera progreso incluso si el flujo de error estándar no se dirige a un terminal. 
-4 
--ipv4 
Usar sólo direcciones IPv4, haciendo caso omiso de las direcciones IPv6. 
-6 
--ipv6 
El uso de direcciones IPv6 solamente, haciendo caso omiso de las direcciones IPv4. 
<Repositorio> 
El repositorio "a distancia", que es la fuente de una operación de extracción o tirar. Este parámetro puede ser una dirección URL (véase la sección de las direcciones URL GIT abajo) o el nombre de un mando a distancia (ver la sección de mandos a distancia más abajo). 
<Refspec> 
Especifica los árbitros para ir a buscar, y que los árbitros locales para actualizar. Cuando no hay <refspec> s aparecerá en la línea de comandos, las referencias a buscar se leen de remote.<repository>.fetch variables en lugar (ver git-fetch [1] ). 
El formato de un parámetro <refspec> es un signo opcional de + , seguido por el árbitro fuente <src>, seguido de dos puntos : , seguido por el árbitro con destino <dst>. El colon se puede omitir cuando <dst> está vacía. 
tag <tag> significa lo mismo que refs/tags/<tag>:refs/tags/<tag> ; pide ir a buscar todo lo que hasta la etiqueta dada. 
El árbitro remoto que coincide con <src> es exagerado, y si <dst> no es una cadena vacía, el árbitro local que coincide que avanza rápidamente usando <src>. Si el signo opcional de + se utiliza, se actualiza el árbitro local, aún si no se traduce en una actualización de avance rápido. 
Nota 	Cuando la rama remota que se desea obtener es conocido por ser rebobinado y porcentualizada regularidad, se espera que su nueva punta no será descendiente de su extremidad anterior (como se almacena en su sucursal de seguimiento a distancia la última vez que exagerado). Que se quiere utilizar el + signo para indicar serán necesarias actualizaciones que no son de avance rápido para estas ramas. No hay manera de determinar o declarar que una rama se pondrá a disposición en un repositorio con este comportamiento; el usuario simplemente tirando debe saber que este es el patrón de uso esperado para una rama. 
Nota 	Hay una diferencia entre el listado múltiple <refspec> directamente en la línea de comandos git tirón y que tiene múltiples remote.<repository>.fetch entradas en su configuración para un <repositorio> y ejecutar un comando git pull sin ningún <> refspec parámetros explícitos. <Refspec> s que aparece explícitamente en la línea de comandos siempre se fusionan en la rama actual después de obtenerlo. En otras palabras, si la lista de más de un árbitro con mando a distancia, git pull creará una combinación de pulpo. Por otro lado, si usted no incluye ningún parámetro explícito <refspec> en la línea de comandos, git pull obtendrá toda la <refspec> s que encuentra en el remote.<repository>.fetch configuración y fusionar sólo el primer <refspec > encontrado en la rama actual. Esto se debe hacer un pulpo de referencias remotas se realiza con poca frecuencia, mientras que el seguimiento de múltiples cabezas remotas en una sola ir por ir a buscar más de uno es a menudo útil.


git push: Actualizaciones referencias remotas utilizando árbitros locales, mientras que el envío de objetos necesarios para completar las referencias dadas.

git push [--all |  --mirror |  --tags] [--follow-tags] [--atomic] [-n |  --dry de gestión] [--receive-pack = <git-recibir-pack>]
	    [--repo = <Repositorio>] [-f |  --force] [-d |  --delete] [--prune] [-v |  --verboso]
	    [-u |  --set-aguas arriba] [-opción --push = <cadena>]
	    [- [No-] firmado | --sign = (true | false | Si-pedido)]
	    [--force-Con-lease [= <refname> [: <esperar>]]]
	    [--no-Verificar] [<repositorio> [<refspec> ...]] 

OPCIONES 
<Repositorio> 
El repositorio "a distancia", que es el destino de una operación de empuje. Este parámetro puede ser una dirección URL (véase la sección de las direcciones URL GIT abajo) o el nombre de un mando a distancia (ver la sección de mandos a distancia más abajo). 
<Refspec> ... 
Especifique lo ref destino para actualizar con lo objeto de origen. El formato de un parámetro <refspec> es un signo opcional de + , seguido del objeto de origen <src>, seguido de dos puntos : , seguido por el árbitro con destino <dst>. 
La <src> es a menudo el nombre de la rama que se quiere impulsar, pero puede ser cualquier "SHA-1 de expresión" arbitraria, como master~4 o HEAD (ver gitrevisions [7] ). 
La <dst> dice qué ref por el lado opuesto se actualiza con este empuje. expresiones arbitrarias no se pueden utilizar aquí, un ref real debe ser nombrado. Si git push [<repository>] sin ninguna <refspec> argumento está configurado para actualizar algunos ref en el destino con <src> con remote.<repository>.push Variable de configuración, :<dst> parte puede ser un omitted- tales empuje actualizará una nevera que <src> normalmente actualiza sin ningún <refspec> en la línea de comandos. De lo contrario, la falta de :<dst> significa actualizar la misma ref como el <src> . 
El objeto referenciado por <src> se utiliza para actualizar la referencia <dst> en el lado remoto. Por defecto esto sólo se permite si <dst> no es una etiqueta (anotado o ligera), y luego sólo si se puede avanzar rápidamente <dst>. Al tener el líder opcional + , se puede decir Git para actualizar el <dst> ref incluso si no está permitido por defecto (por ejemplo, no es un avance rápido.) Esto no pretende fusionar <src> en <dst >. Ver ejemplos a continuación para más detalles. 
tag <tag> significa lo mismo que refs/tags/<tag>:refs/tags/<tag> . 
Empujar a un vacío <src> le permite borrar el <dst> ref desde el repositorio remoto. 
El refspec especial : (o +: para permitir actualizaciones no avance rápido) dirige Git para empujar ramas "igualación": por cada rama que existe en el lado local, el lado remoto se actualiza si una rama del mismo nombre ya existe en el lado remoto. 
--todas 
Empujar todas las ramas (por ejemplo, refs bajo refs/heads/ ); no se puede utilizar con otro <refspec>. 
--ciruela pasa 
Quite las ramas remotas que no cuentan con una contraparte local. Por ejemplo, una rama remota tmp se eliminará si una rama local con el mismo nombre no existe más. Esto también respeta refspecs, por ejemplo, git push --prune remote refs/heads/*:refs/tmp/* se aseguraría de que remota refs/tmp/foo se eliminará si refs/heads/foo no existe. 
--espejo 
En lugar de nombrar cada árbitro empujar, especifica que todos los árbitros en virtud de refs/ (que incluye pero no se limita a refs/heads/ , refs/remotes/ y refs/tags/ ) se reflejarán en el repositorio remoto. árbitros locales de nueva creación serán empujados al extremo remoto, referencias actualizadas a nivel local se actualizan fuerza en el extremo remoto y árbitros borrados se eliminan del extremo remoto. Este es el valor predeterminado si la opción de configuración remote.<remote>.mirror se establece. 
-norte 
--dry de gestión 
Hacer todo excepto en realidad enviar las actualizaciones. 
--porcelana 
Producir una salida legible por máquina. La línea de estado de salida para cada árbitro será separado por tabuladores y se envía a la salida estándar en lugar de stderr. La entrega de los nombres simbólicos completos de los árbitros. 
--borrar 
Todas las referencias que figuran se eliminan del repositorio remoto. Este es el mismo que el prefijo todas las refs con dos puntos. 
--tags 
Todos los árbitros en virtud refs/tags son empujadas, además de refspecs enumerados explícitamente en la línea de comandos. 
--follow-tags 
Empuje todos los árbitros que puedan empujar sin esta opción, y también enviar etiquetas anotadas en refs/tags que faltan en el mando a distancia, pero apuntan a cometer-ish que son accesibles desde los árbitros siendo empujadas. Esto también se puede especificar con variables de configuración push.followTags . Para obtener más información, consulte push.followTags en git-config [1] . 
- [No-] firmado 
--sign = (true | false | Si-pedido) 
GPG-firmar la solicitud de inserción para actualizar los árbitros en el lado de recepción, para que pueda ser verificado por los ganchos y / o iniciar sesión. Si false o --no-signed , se intentará ninguna firma. Si true o --signed , el empuje fallará si el servidor no soporta empujones firmados. Si se fija en if-asked , firmar si y sólo si el servidor soporta empujones firmados. El empuje también fallará si la llamada real a gpg --sign falla. Ver git-recibir-pack [1] para los detalles en el extremo receptor. 
- [No-] atómica 
Utilice una transacción atómica en el lado remoto si está disponible. O todos los árbitros se actualizan, o en caso de error, no hay referencias se actualizan. Si el servidor no soporta el empuje empujes atómicas fallará. 
-O 
-Opción --push 
Transmitir la cadena dada al servidor, lo que les pasa a la pre-recibir, así como el gancho post-recibir. La cadena dada no debe contener un carácter NUL o LF. 
--receive-pack = <git-recibir-pack> 
--exec = <git-recibir-pack> 
Ruta de acceso al programa de git-recibir-pack en el extremo remoto. A veces resulta útil cuando se empuja a un repositorio remoto a través de ssh, y usted no tiene el programa en un directorio predeterminado en el $ PATH. 
- [No-] fuerza-con-arrendamiento 
--force-con-lease = <refname> 
--force-con-lease = <refname>: <esperar> 
Por lo general, "git push" se niega a actualizar una referencia remota que no es un antepasado de que el árbitro local utilizado para sobrescribirlo. 
Esta opción anula esta restricción si el valor actual de la ref remoto es el valor esperado. "Git push" no lo contrario. 
Imagínese que usted tiene que rebase lo que ya han publicado. Usted tendrá que pasar por alto la norma "debe avanzar rápidamente" con el fin de sustituir la historia se publicó originalmente con la historia rebasada. Si alguien construye encima de su historia original, mientras que usted está rebasado, la punta de la rama en el mando a distancia puede avanzar con su cometido, y ciegamente empujando con --force perderá su trabajo. 
Esta opción le permite decir que usted espera que la historia va a actualizar lo que es rebasada y desea reemplazar. Si el árbitro remota todavía señala en el envío de datos que ha especificado, puede estar seguro de que no hay otras personas hicieron nada para que el árbitro. Es como tomar un "arrendamiento" en la que el árbitro sin bloquear de forma explícita, y que el árbitro remota sólo se actualiza si el "arrendamiento" sigue siendo válida. 
--force-with-lease solo, sin especificar los detalles, protegerá a todos los árbitros remotos que van a ser actualizados al exigir su valor actual a ser la misma que la rama de seguimiento a distancia que tenemos para ellos. 
--force-with-lease=<refname> , sin especificar el valor esperado, protegerá al árbitro nombrado (solo), si va a ser actualizado, al exigir su valor actual a ser la misma que la rama de seguimiento remoto tenemos para ello. 
--force-with-lease=<refname>:<expect> protegerá al árbitro nombrado (solo), si va a ser actualizado, al exigir su valor actual a ser el mismo que el valor especificado <expect> (que se permite que sea diferente de la rama remota de seguimiento que tenemos para el refname, o que ni siquiera tiene que tener una sucursal de las características de seguimiento a distancia cuando se utiliza este formulario). Si <expect> es la cadena vacía, entonces no debe existir ya que el árbitro nombrado. 
Tenga en cuenta que todas las formas distintas de --force-with-lease=<refname>:<expect> que especifica el valor actual esperado de la ref son explícitamente todavía experimental y su semántica pueden cambiar a medida que ganamos experiencia con esta característica. 
"--no-Fuerza-con-arrendamiento", se cancelará toda la --force-con-arrendamiento de la línea de comandos anterior. 
-F 
--fuerza 
Por lo general, el comando se niega a actualizar una referencia remota que no es un antepasado de que el árbitro local utilizado para sobrescribirlo. Además, cuando --force-with-lease se utiliza la opción, el comando se niega a actualizar una referencia a distancia cuyo valor actual no coincide con lo que se espera. 
Esta opción deshabilita estas comprobaciones, y puede hacer que el repositorio remoto a perder commit; usarlo con cuidado. 
Tenga en cuenta que --force se aplica a todos los árbitros que son empujados, por lo tanto, se utiliza con push.default establecido en matching o con múltiples destinos empuje configurados con remote.*.push puede sobrescribir árbitros distintos de la rama actual (incluyendo referencias locales que están estrictamente detrás de su homólogo remoto). Para forzar un empuje a una sola rama, utilizar un + delante de la refspec para empujar (por ejemplo, git push origin +master para forzar un empuje a la master rama). Ver el <refspec>... sección anterior para más detalles. 
--repo = <repositorio> 
Esta opción es equivalente a la <repositorio> argumento. Si se especifican ambos, el argumento de línea de comandos tiene precedencia. 
-u 
--set-aguas arriba 
Para todo aquel que esté actualizada o empujado con éxito, añadir aguas arriba de referencia (seguimiento), utilizado por el argumento menos git-pull [1] y otros comandos. Para obtener más información, consulte la branch.<name>.merge en git-config [1] . 
- [No-] delgada 
Estas opciones se pasan a git-send-pack [1] . Una transferencia delgada reduce significativamente la cantidad de datos enviados cuando el emisor y el receptor comparten muchos de los mismos objetos en común. El valor predeterminado es \ - delgada. 
-q 
--tranquilo 
Suprimir todas las salidas, incluyendo la lista de referencias actualizadas, a menos que se produzca un error. El progreso no se informa a la secuencia de error estándar. 
-v 
--verboso 
Correr más detallados. 
--Progreso 
estado de progreso se informó sobre la secuencia de error estándar de forma predeterminada cuando está conectado a un terminal, a menos que se especifique -q. Este estado fuerzas bandera progreso incluso si el flujo de error estándar no se dirige a un terminal. 
--no-recurse-submódulos 
--recurse-submódulos = comprobar | On-Demand | no 
Se puede utilizar para asegurarse de que todas las confirmaciones submódulo utilizado por las revisiones al ser empujado están disponibles en una rama de seguimiento remoto. Si se utiliza Git cheque verificará que todos los envíos submódulo que cambiaron en las revisiones para ser empujado están disponibles en al menos una distancia del submódulo. Si ningún commit faltan el empuje será abortado y el estado de salida distinto de cero. Si se utiliza a la carta todos los submódulos que cambiaron en las revisiones para ser empujado será empujado. Si en la demanda no era capaz de empujar todas las revisiones necesarias también será abortado y el estado de salida distinto de cero. Un valor de no uso o --no-recurse-submodules se puede utilizar para anular la variable de configuración push.recurseSubmodules cuando no se requiere la recursividad submódulo. 
- [No-] verificar 
Mueva el gancho pre-push (ver githooks [5] ). El valor predeterminado es --verify, dándole al gancho una oportunidad para evitar el empuje. Con --no-Verify, el gancho se omite por completo. 
-4 
--ipv4 
Usar sólo direcciones IPv4, haciendo caso omiso de las direcciones IPv6. 
-6 
--ipv6 
El uso de direcciones IPv6 solamente, haciendo caso omiso de las direcciones IPv4. 
Ejemplos

git push

    Funciona como git push <remote> , donde <distancia> es remota (o de la rama actual origin , si no había control remoto está configurado para la rama actual). 
git push origin

    Sin necesidad de configuración adicional, empuja la rama actual a la corriente arriba (configurado remote.origin.merge configuración variable) si tiene el mismo nombre que la rama actual, y los errores sin haberla empujado lo contrario.

    El comportamiento predeterminado de este comando cuando hay <refspec> viene dada puede configurarse estableciendo el push opción de la distancia o el push.default variable de configuración.

    Por ejemplo, por defecto a empujar solamente la rama actual de origin uso git config remote.origin.push HEAD . Cualquier válida <refspec> (como los de los ejemplos a continuación) se pueden configurar como predeterminado para git push origin . 
git push origin :

    Empuje ramas "igualación" a origin . Consulte <refspec> en el OPCIONES sección anterior para una descripción de las ramas "igualación". 
git push origin master

    Encuentra una referencia que coincide con master en el repositorio de código fuente (lo más probable, sería encontrar refs/heads/master ), y actualizar la misma referencia (por ejemplo, refs/heads/master ) en el origin repositorio con ellos. Si master no existía de forma remota, se crearía. 
git push origin HEAD

    Una manera práctica de empujar la rama actual con el mismo nombre en el mando a distancia. 
git push mothership master:satellite/master dev:satellite/dev

    Utilice el árbitro fuente que coincide master (por ejemplo, refs/heads/master ) para actualizar el árbitro que coincide satellite/master (muy probablemente refs/remotes/satellite/master ) en la mothership repositorio; hacer lo mismo para dev y satellite/dev .

    Se trata de emular git fetch ejecuta en el mothership usando git push que se ejecuta en la dirección opuesta con el fin de integrar el trabajo realizado sobre satellite , y es a menudo necesario cuando sólo se puede hacer la conexión de una forma (es decir satélite puede ssh en nodriza pero nodriza no puede iniciar la conexión al satélite ya que este último está detrás de un firewall o no corre sshd).

    Después de ejecutar este git push en el satellite de la máquina, que le ssh en la mothership y ejecutar git merge allí para completar la emulación de git pull que se ejecuta en mothership para tirar de los cambios realizados en el satellite . 
git push origin HEAD:master

    Empuje la rama actual a la distancia ref juego master en el origin repositorio. Esta forma es conveniente para empujar la rama actual sin pensar en su nombre local. 
git push origin master:refs/heads/experimental

    Crear la rama experimental en el origin repositorio copiando la corriente master rama. Este formulario sólo se necesita para crear una nueva rama o una etiqueta en el repositorio remoto cuando el nombre local y el nombre remoto son diferentes; de lo contrario, el nombre ref por sí solo va a funcionar. 
git push origin :experimental

    Encuentra una referencia que coincide experimental en el origin del repositorio (por ejemplo, refs/heads/experimental ), y eliminarlo. 
git push origin +dev:master

    . Modificar una rama principal del repositorio de origen con la rama dev, permitiendo actualizaciones no avance rápido Esto puede hacer commit no referenciados que cuelgan en el repositorio de origen Considere la siguiente situación, donde un avance rápido no es posible.:

      o --- o --- o --- A --- B origen / maestra
    		      \
    		       X --- Y --- Z dev 

    El comando anterior cambiaría el repositorio de origen hasta

      A --- B (branch sin nombre)
    		      /
    	     o --- o --- o --- X --- Y --- Z maestro 

    Se compromete A y B ya no pertenecería a una rama con un nombre simbólico, y así sería inalcanzable. Como tal, estas confirmaciones se eliminarían por un git gc comando en el repositorio de origen.


git checkout:  Actualizaciones de los archivos en el directorio de trabajo para que coincida con la versión en el índice o el árbol especificado. Si no se dan caminos, git checkout también actualizará HEAD para establecer la rama especificada como la rama actual.

 git checkout [q] [-f] [-m] [<branch>]
 git checkout [q] [-f] [-m] --detach [<branch>]
 git checkout [q] [-f] [-m] [--detach] <cometer>
 git checkout [q] [-f] [-m] [[-b | -B | --orphan] <new_branch>] [<punto_de_inicio>]
 git checkout [-f | --ours | --theirs | -m | --conflict = <style>] [<-ish árbol>] [-] <> caminos ...
 git checkout [-p | --patch] [<-ish árbol>] [-] [<caminos> ...] 

git checkout <branch> 
Para prepararse para trabajar en <branch>, cambiar a ella mediante la actualización del índice y los archivos en el directorio de trabajo, y señalando la cabeza ante la rama. modificaciones locales a los archivos en el directorio de trabajo se mantienen, de manera que puedan estar comprometidos con el <branch>. 
Si <branch> no se encuentra, pero sí que existe una rama de seguimiento en exactamente una distancia (llamarlo <remote>) con un nombre coincidente, asimilar a 
  $ Git checkout -b <branch> --track <remote> / <branch> 
Se podría omitir <branch>, en cuyo caso el comando degenera en "echa un vistazo a la rama actual", que es un glorificado no-op con bastante caros efectos secundarios para mostrar sólo la información de seguimiento, si existe, de la rama actual . 
git checkout --detach [<branch>] 
git checkout [--detach] <cometer> 
Prepárese para trabajar en la parte superior de <cometer>, separando la cabeza ante él (véase la sección "cabeza separada"), y actualizar el índice y los archivos en el directorio de trabajo. modificaciones locales a los archivos en el directorio de trabajo se mantienen, por lo que el árbol de trabajo resultante será el estado grabado en el envío de datos, además de las modificaciones locales. 
Cuando el <cometer> argumento es un nombre de la sucursal, el --detach opción se puede utilizar para separar la cabeza ante la punta de la rama ( git checkout <branch> se echa un vistazo a esa rama sin separar HEAD). 
Omitiendo <branch> CABEZA separa en la punta de la rama actual. 
git checkout [-p | --patch] [<-ish árbol>] [-] <pathspec> ... 
Cuando <caminos> o --patch se dan, git checkout no cambia ramas. Se actualiza los caminos con nombre en el directorio de trabajo del archivo de índice o de un llamado <árbol-ish> (lo más a menudo una confirmación). En este caso, el -b y --track opciones no tienen sentido y dando a ninguno de ellos da lugar a un error. La <tree-ish> argumento puede ser utilizado para especificar un árbol-ish específica (es decir, se comprometen, etiqueta o árbol) para actualizar el índice de las rutas proporcionadas antes de actualizar el árbol de trabajo. 
git checkout con <caminos> o --patch se utiliza para restaurar caminos modificados o eliminados de sus contenidos originales del índice o reemplazar caminos con el contenido de un llamado <árbol-ish> (lo más a menudo un ish-comprometerse). 
El índice puede contener entradas sin combinar debido a una fusión fallida anterior. Por defecto, si se intenta retirar dicha entrada del índice, la operación de pago se producirá un error y nada será desprotegido. El uso de -f ignorará estas entradas no combinadas. El contenido de uno de los lados de la fusión se pueden sacar del índice utilizando --ours o --theirs . Con -m , los cambios realizados en el archivo árbol de trabajo pueden ser descartados para volver a crear el resultado de la combinación original de conflicto. 
OPCIONES 
-q 
--tranquilo 
Tranquila, suprimir los mensajes de retroalimentación. 
--[sin progreso 
Estado de progreso se informó sobre la secuencia de error estándar de forma predeterminada cuando está conectado a un terminal, a menos que --quiet se especifica. Este indicador permite a los informes de progreso, incluso si no conectado a un terminal, independientemente de --quiet . 
-F 
--fuerza 
Cuando se cambia ramas, continúe incluso si el índice o el árbol de trabajo difiere de HEAD. Esto se utiliza para tirar a la basura los cambios locales. 
Al momento de pagar caminos del índice, no dejan a las entradas no combinadas; en cambio, las entradas no combinadas se ignoran. 
--la nuestra 
--suyo 
Al momento de pagar rutas desde el índice, echa un vistazo a la etapa # 2 (la nuestra) o # 3 (el suyo) para los caminos sin combinar. 
Tenga en cuenta que durante git rebase y git pull --rebase , la nuestra y la de ellos pueden aparecer intercambiado; --ours da la versión de la rama de los cambios se restablecen a, mientras que --theirs da la versión de la rama que lleva a cabo su trabajo que es siendo rebasada. 
Esto se debe a que rebase se utiliza en un flujo de trabajo que trata la historia en el mando a distancia como la canónica compartida, y trata el trabajo realizado en la rama que se rebase como el trabajo de terceros para ser integrado, y que están asumiendo temporalmente la función de la meta de la historia canónica durante el rebase. A medida que el guardián de la historia canónica, tiene que ver la historia desde el mando a distancia como ours (es decir, "nuestra compartida historia canónica"), mientras que lo que hizo en su rama lateral como theirs (es decir, "el trabajo de un colaborador en la parte superior de la misma" ). 
-b <new_branch> 
Crear una nueva rama llamada <new_branch> e iniciarlo a <punto_de_inicio>; 
-B <New_branch> 
Crea la rama <new_branch> y empezar a que a <punto_de_inicio>; si ya existe, a continuación, restablecerlo a <punto_de_inicio>. Esto es equivalente a ejecutar "git branch" con "f".


-t 
--pista 
Al crear una nueva rama, configurar la configuración de "aguas arriba". Consulte "--track" en git-rama [1] para más detalles. 
Si no -b se da opción, el nombre de la nueva rama se deriva de la rama de seguimiento remoto, mirando a la parte local de la refspec configurado para la distancia correspondiente, y luego separar el parte inicial hasta la "* ". Esto nos diría que utilizar "cortar" como la rama local cuando se desvía de "origen / truco" (o "controles remotos / origen / piratear", o incluso "refs / mandos a distancia / origen / hack"). Si el nombre que se da sin barra, o por encima de los resultados de adivinanzas en un nombre vacío, la conjetura es abortada. Se puede dar un nombre explícitamente con -b en tal caso. 
--no hay pista 
No instale la configuración "aguas arriba", incluso si la variable de configuración branch.autoSetupMerge es cierto. 
-l 
Crear reflog de la nueva sucursal; ver git-rama [1] para más detalles. 
--despegar 
En lugar de retirar una rama que trabajar en ello, echa un vistazo a una confirmación para la inspección y experimentos descartables. Este es el comportamiento por defecto de "git checkout <cometer>" cuando <cometer> no es un nombre de la sucursal. Vea la sección de "cabeza separada" a continuación para más detalles. 
--orphan <new_branch> 
Crear una nueva rama huérfano, llamado <new_branch>, comenzado desde <punto_de_inicio> y cambiar a ella. El primer commit hecho en esta nueva rama no tendrá ningún padres y que será la raíz de una nueva historia totalmente desconectado de todas las otras ramas y se compromete. 
El índice y el árbol de trabajo se adaptan, como si se hubiera ejecutado anteriormente "git checkout <punto_de_inicio>". Esto le permite iniciar una nueva historia que registra un conjunto de rutas similares a <punto_de_inicio> ejecutando fácilmente "git commit -a" para hacer la raíz cometió. 
Esto puede ser útil cuando se desea publicar el árbol a partir de una confirmación sin exponer toda su historia. Es posible que desee hacer esto para publicar una rama de código abierto de un proyecto cuya corriente árbol es "limpia", pero cuyo historial completo contiene bits de propiedad o de otro modo gravados de código. 
Si desea iniciar una historia desconectado que registra un conjunto de caminos que es totalmente diferente a la de <punto_de_inicio>, entonces usted debe borrar el índice y el árbol de trabajo justo después de la creación de la rama huérfano ejecutando "git rm-rf. " desde el nivel superior del árbol de trabajo. Después, estará listo para preparar sus nuevos archivos, repoblar el árbol de trabajo, copiándolos desde otro lugar, la extracción de un archivo comprimido, etc. 
--ignore-skip-worktree-bits 
En el modo de pago y envío escasa, git checkout -- <paths> actualizaría solo las entradas coincidentes por caminos <> y patrones dispersos en $ GIT_DIR / info / escasa-checkout. Esta opción pasa por alto los patrones dispersos y vuelve a agregar los archivos en <caminos>. 
-metro 
--unir 
Cuando se cambia ramas, si tiene modificaciones locales a uno o más archivos que son diferentes entre la rama actual y la rama a la que usted está cambiando, el comando se niega a cambiar las ramas con el fin de preservar sus modificaciones en su contexto. Sin embargo, con esta opción, una de tres vías de combinación entre la rama actual, el contenido de su árbol de trabajo, y la nueva rama se hace, y usted estará en la nueva rama. 
Cuando ocurre un conflicto de combinación, las entradas de índice para caminos en conflicto se dejan sin combinar, y que necesita para resolver los conflictos y marcar los caminos resueltos con git add (o git rm si la fusión debe dar lugar a la supresión de la ruta). 
Al momento de pagar caminos del índice, esta opción le permite recrear la combinación de conflicto en las rutas especificadas. 
--conflict = <style> 
Lo mismo que --merge opción anterior, pero cambia la forma en que se presentan los trozos en conflicto, anulando la variable de configuración merge.conflictStyle. Los valores posibles son "fusión" (por defecto) y "diff3" (además de lo que se desprende de "fusionar" estilo, muestra el contenido original). 
-pag 
--parche 
Interactivamente seleccionar trozos en la diferencia entre el <árbol-ish> (o el índice, si no se especifica) y el árbol de trabajo. Los trozos escogidos A continuación se aplican a la inversa para el árbol de trabajo (y si a <árbol-ish> se ha especificado, el índice). 
Esto significa que se puede utilizar git checkout -p para descartar selectivamente ediciones de su árbol de trabajo actual. Vea la sección "Modo interactivo" de git-add [1] para aprender cómo operar el --patch modo. 
--ignore-otras-worktrees 
git checkout se niega cuando el árbitro deseada ya está desprotegido por otro worktree. Esta opción hace que compruebe que el árbitro de todos modos. En otras palabras, el árbitro puede ser ocupado por más de una worktree. 
<Branch> 
Rama a la caja; si se refiere a una rama (es decir, un nombre que, cuando precedidas por "refs / heads /", es una referencia válida), entonces esa rama está desprotegido. De lo contrario, si se refiere a una confirmación válida, la cabeza se convierte en "independiente" y que ya no está en cualquiera de las ramas son (ver más abajo para más detalles). 
Como caso especial, la "@{-N}" sintaxis de la última rama N-th / cometen cheques ramas (en lugar de quitar). También puede especificar - que es sinónimo de "@{-1}" . 
Como caso especial adicional, puede utilizar "A...B" como un acceso directo a la base de mezcla de A y B si hay exactamente una base de combinación. Usted puede dejar de lado a lo sumo uno de A y B , en cuyo caso el valor predeterminado es HEAD . 
<New_branch> 
Nombre para la nueva rama. 
<Punto_de_inicio> 
El nombre de una cometen en que debe comenzar la nueva rama; ver git-rama [1] para más detalles. Por defecto es la cabeza. 
<Tree-ish> 
Árbol desde la que obtener (cuando se dan caminos). Si no se especifica, se utilizará el índice. 

EJEMPLOS 
1.	La siguiente secuencia cabo controles de la master rama, revierte el Makefile a dos revisiones espalda, elimina hola.c por error, y se pone de nuevo a partir del índice. 
2.	  $ Git checkout master (1)
3.	 $ Git checkout master ~ 2 Makefile (2)
4.	 $ Rm -f hola.c
 $ Git checkout hola.c (3) 
1.	rama conmutador 
2.	llevar a cabo un archivo de otro cometen 
3.	restaurar hola.c del índice 
Si quieres echa un vistazo a todos los archivos de origen C fuera del índice, se puede decir 
  $ Git checkout - '* .c' 
Tenga en cuenta las comillas *.c . El archivo hello.c también estará desprotegido, a pesar de que ya no está en el directorio de trabajo es, debido a que la expansión de nombres de archivo se utiliza para que coincida con las entradas en el índice (no en el árbol de trabajo por el shell). 
Si usted tiene una rama desafortunado que se denomina hello.c , este paso sería confundida como una instrucción para cambiar a esa rama. En su lugar debe escribir: 
  $ Git checkout - hola.c 
5.	Después de trabajar en la rama equivocada, el cambio a la rama correcta se llevaría a cabo mediante: 
  $ Git checkout MyTopic 
Sin embargo, su rama rama "equivocado" y "MyTopic" correcta puede ser diferente en los archivos que ha modificado localmente, en cuyo caso el pago y envío anterior podría fallar de esta manera: 
  $ Git checkout MyTopic
 Error: Tiene cambios locales a 'Frotz';  No conmutación ramas. 
Se puede dar el -m bandera para el comando, lo que intentar una fusión a tres bandas: 
  $ Git checkout -m MyTopic
 Auto-fusión Frotz 
Después de esto a tres bandas de combinación, las modificaciones locales no están registrados en el archivo de índice, por lo git diff que le indicará a qué cambios realizados desde la punta de la nueva rama. 
6.	Cuando un conflicto de combinación que ocurre durante la conmutación ramas con el -m opción, que se vería algo como esto: 
7.	  $ Git checkout -m MyTopic
8.	 Auto-fusión Frotz
9.	 ERROR: Combinar conflicto en Frotz
 fatal: programa de fusión fracasó 
En este punto, git diff muestra los cambios limpiamente fusionados como en el ejemplo anterior, así como los cambios en los archivos en conflicto. Editar y resolver el conflicto y la marca se resolvió con git add como de costumbre: 
  $ Editar Frotz
 $ Git add Frotz 

git add: Para empezar el seguimiento de un nuevo archivo.
Iniciaremos el seguimiento del archivo README ejecutando esto:
$ git add README

git checkout -b "nombre": 
git checkout -b | -B <new_branch> [<punto de comenzar>] 
Especificando -b provoca una nueva rama que se creará como si git-rama [1] se llama y luego desprotegido. En este caso se pueden utilizar las --track o --no-track opciones, que serán pasados a git rama. Como ventaja, --track sin -b implica la creación de sucursal; ver la descripción de --track a continuación. 
Si -B se da, <new_branch> se crea si no existe; de lo contrario, se restablece. Esto es el equivalente de transaccional 
  $ Git branch -f <branch> [<Punto inicial>]
 $ Git checkout <branch> 
es decir, la rama no se restablece / creado a menos que "git checkout" es un éxito. 

git commit -am"primer commit": Si haces de nuevo un comando "git status" podrás comprobar que no hay nada para enviar al repositorio. Eso quiere decir que la zona de Index está limpia y que todos los cambios están enviados a Git. 
Hasta este punto hemos podido aprender a crear nuestro repositorio y enviar los primeros cambios por medio de la operación de commit. Ahora puedes probarlo en tu sistema para comenzar a experimentar Git.
git commit -m "mensaje para el commit"

git pull rebase: Incorpora cambios con respecto a un repositorio remoto en la rama actual. En su modo predeterminado, git pull es la abreviatura de git fetch seguido por git merge FETCH_HEAD . 
Más precisamente, git pull ejecuta git fetch con los parámetros dados y llama git merge para combinar los directores de las sucursales recuperados en la rama actual. Con --rebase , se ejecuta git rebase en lugar de git merge. 
<repositorio> debe ser el nombre de un repositorio remoto como los pasados a git-fetch [1] . <Refspec> puede nombrar a un árbitro a distancia arbitraria (por ejemplo, el nombre de una etiqueta) o incluso una colección de referencias con ramas de seguimiento remoto correspondiente (por ejemplo, refs / heads / *: refs / mandos a distancia / origen / *), pero por lo general, es el nombre de una rama en el repositorio remoto. 
Los valores por defecto para <repositorio> y <branch> se lee de la "distancia" y "fusionar" la configuración de la rama actual según lo establecido por git-rama [1] --track . 
git pull [opciones] [<repositorio> [<refspec> ...]] 

OPCIONES

-q
--tranquilo

    Esto se pasa al tanto que subyace git-fetch para aplastar a la presentación de informes de durante el traslado y subyacente git-fusión para aplastar salida durante la fusión. 
-v
--verboso

    Pase al --verbose git-fetch y git-fusión. 
- [No-] recurse-submódulos [= yes | On-Demand | no]

    Esta opción controla si las nuevas confirmaciones de todos los submódulos pobladas deben captarse también (ver git-config [1] y gitmodules [5] ). Eso podría ser necesaria para obtener los datos necesarios para la fusión submódulo se compromete, una característica Git aprendido en 1.7.3. Observe que el resultado de una fusión no se comprobará en el submódulo "actualización git submódulo" tiene que ser llamado después para llevar el árbol de trabajo hasta la fecha con el resultado de la fusión. 

Opciones relacionadas con la fusión

--cometer
--no-commit

    Realizar la combinación y comprometer el resultado. Esta opción se puede utilizar para anular --no-commit.

    Con --no-commit realizar la combinación, pero pretender que la fusión fallida y no confirmación automática, para dar al usuario la oportunidad de inspeccionar y modificar el resultado de la fusión antes de comprometerse aún más. 
--editar
-mi
--sin editar

    Invocar un editor antes de comprometer el éxito de combinación mecánica para modificar aún más el mensaje de mezcla generada automáticamente, de modo que el usuario puede explicar y justificar la fusión. El --no-edit opción se puede utilizar para aceptar el mensaje de auto-generado (esto se suele desalentar).

    guiones de edad avanzada pueden depender del comportamiento histórico de no permitir al usuario editar el mensaje de registro de fusión. Ellos verán un editor abierto cuando se ejecutan git merge . Para que sea más fácil para ajustar dichas secuencias de comandos para el comportamiento actualizado, la variable de entorno GIT_MERGE_AUTOEDIT se puede configurar para no al comienzo de ellos. 
--ff

    Cuando la fusión se resuelve como un avance rápido, sólo se actualizará el puntero rama, sin crear una fusión cometió. Este es el comportamiento predeterminado. 
--no-ff

    Crear una combinación de cometer incluso cuando la fusión se resuelve como un avance rápido. Este es el comportamiento por defecto cuando la fusión de una anotada (y posiblemente firmado) etiqueta. 
--ff de sólo

    Negarse a fusionar y salida con un estado distinto de cero a menos que el actual HEAD es ya hasta a la fecha o la combinación puede ser resuelto como un avance rápido. 
--log [= <n>]
--no-log

    Además de los nombres de rama, poblar el mensaje de registro con las descripciones de una línea de en la mayoría de <n> commit reales que se están fusionadas. Ver también git-fmt-merge-msg [1] .

    Con --no-log no anotar las descripciones de una sola línea de las confirmaciones reales se fusione. 
--stat
-norte
--no-stat

    Mostrar una diffstat al final de la fusión. El diffstat también es controlado por la opción de configuración merge.stat.

    Con -n o --no-stat no muestran una diffstat al final de la fusión. 
--squash
--no-calabaza

    Producir el estado del árbol y el índice de trabajo como si una verdadera fusión ocurrió (a excepción de la información de combinación), pero en realidad no hacen un commit, mover la HEAD , o registro $GIT_DIR/MERGE_HEAD (para hacer que el próximo git commit comando para crear una fusionar comprometerse). Esto le permite crear una única confirmación en la parte superior de la rama actual, cuyo efecto es el mismo que la fusión de otra rama (o más en caso de un pulpo).

    Con --no-calabaza realizar la combinación y comprometer el resultado. Esta opción se puede utilizar para anular --squash. 
-s <estrategia>
--strategy = <estrategia>

    Utilizar la estrategia de combinación dada; se pueden suministrar más de una vez para especificar en el orden en que deben ser juzgados. Si no hay -s opción, una lista integrada de las estrategias se utiliza en su lugar (git merge-recursiva cuando la fusión de una sola cabeza, git merge-pulpo de otro modo). 
-X <Opción>
-Opción --strategy = <opción>

    Pasar opción específica estrategia de combinación a través de la estrategia de combinación. 
--verify firmas
-firmas --no-verificar

    Verificar que la punta de cometer la rama lateral está fusionando está firmado con una clave válida, es decir, una llave que tiene un fluido válida: en el modelo de confianza predeterminado, esto significa que la clave de firma ha sido firmada por una clave de confianza. Si la punta de cometer la rama lateral no está firmado con una clave válida, la fusión se aborta. 
--resumen
--no-Resumen

    Los sinónimos para --stat y --no-stat; éstos están en desuso y se eliminará en el futuro. 
--allow-no relacionadas-historias

    De forma predeterminada, git merge comando se niega a fusionar historias que no comparten un ancestro común. Esta opción se puede utilizar para anular esta seguridad al combinar las historias de dos proyectos que comenzaron su vida de forma independiente. Ya que es una ocasión muy rara, hay una variable de configuración para habilitar esto por defecto existe y no se añadirá. 

-r
--rebase [= false | true | preservar | interactiva]

    Cuando es verdadero, rebase la rama actual en la parte superior de la rama ascendente después de obtenerlo. Si hay una rama de seguimiento a distancia correspondiente a la rama aguas arriba y aguas arriba de la rama se reajusta desde el pasado captada, el rebase utiliza esa información para evitar un rebase cambios no locales.

    Cuando se ajusta a preservar, rebase con el --preserve-merges opciones transferida a git rebase de manera que la fusión creada localmente comete no se aplana.

    Cuando falsa, fusionar la rama actual en la rama ascendente.

    Cuando interactive , active el modo interactivo de rebase.

    Ver pull.rebase , branch.<name>.rebase y branch.autoSetupRebase en git-config [1] si desea hacer git pull siempre utilizan --rebase en lugar de combinar.
    Nota
    	Este es un modo potencialmente peligrosa de operación. Se reescribe la historia, que no es un buen augurio cuando publicó que la historia ya. No utilice esta opción a menos que haya leído git-rebase [1] con cuidado. 
--no-rebase

    --rebase Anular anterior. 
--autostash
--no-autostash

    Antes de comenzar el rebase, escondite modificaciones locales de distancia (véase git-alijo [1] ), si es necesario, y aplicar el alijo cuando haya terminado. --no-autostash resulta útil para anular la rebase.autoStash variable de configuración (véase git-config [1] ).

    Esta opción sólo es válida cuando se utiliza "--rebase". 

Opciones relacionadas con ir a buscar

--todas

    Fetch todos los controles remotos. 
-un
--adjuntar

    Anexar al árbitro nombres y nombres de objeto de árbitros captadas que el contenido existente de .git/FETCH_HEAD . Sin esta opción, los datos antiguos en .git/FETCH_HEAD será sobrescrita. 
--depth = <profundidad>

    Limitar ir a buscar al número especificado de confirmaciones de la punta de cada rama de la historia remota. Si ir a buscar a un depósito superficial creada por git clone con --depth=<depth> opción (véase git-clone [1] ), profundizar o acortar la historia al número especificado de confirmaciones. Etiquetas para las confirmaciones profundizadas no se obtendrán. 
--unshallow

    Si el repositorio de código fuente es completa, convertir un depósito superficial para una completa, la eliminación de todas las limitaciones impuestas por los depósitos someros.

    Si el repositorio de código fuente es poco profunda, se ha podido recuperar tanto como sea posible para que el repositorio actual tiene la misma historia como el repositorio de origen. 
--update poco profunda

    Por defecto se deben recuperar desde un repositorio de poca profundidad, git fetch se niega referencias que se tienen que actualizar .git / superficial. Esta opción actualiza .git / superficial y aceptan tales referencias. 
-F
--fuerza

    Cuando se utiliza git fetch con <rbranch>:<lbranch> refspec, se niega a actualizar la rama local <lbranch> menos que el grupo control remoto <rbranch> se obtiene es un descendiente de <lbranch> . Esta opción anula el registro de entrada. 
-k
--guardar

    Mantenga el paquete descargado. 
--no-etiquetas

    Por defecto, las etiquetas que apuntan a objetos que se descargan desde el repositorio remoto se recuperan y se almacenan localmente. Esta opción se desactiva esta siguiente automática de etiquetas. El comportamiento predeterminado de un control remoto puede ser especificado con el mando a distancia. <Nombre> configuración .tagOpt. Ver git-config [1] . 
-u
--update-cabeza-ok

    Por git por defecto se ha podido recuperar niega a actualizar la cabeza que corresponde a la rama actual. Esta opción deshabilita el registro de entrada. Esto es puramente para el uso interno de git pull para comunicarse con git fetch, y, a menos que esté implementando su propia porcelana no se supone para usarlo. 
--upload-pack <carga-pack>

    Cuando se le presente, y el repositorio para ir a buscar a partir es manejado por git fetch-Pack, --exec=<upload-pack> se pasa al comando para especificar la ruta no predeterminada para el comando de marcha en el otro extremo. 
--Progreso

    estado de progreso se informó sobre la secuencia de error estándar de forma predeterminada cuando está conectado a un terminal, a menos que se especifique -q. Este estado fuerzas bandera progreso incluso si el flujo de error estándar no se dirige a un terminal. 
-4
--ipv4

    Usar sólo direcciones IPv4, haciendo caso omiso de las direcciones IPv6. 
-6
--ipv6

    El uso de direcciones IPv6 solamente, haciendo caso omiso de las direcciones IPv4. 

<Repositorio>

    El repositorio "a distancia", que es la fuente de una operación de extracción o tirar. Este parámetro puede ser una dirección URL (véase la sección de las direcciones URL GIT abajo) o el nombre de un mando a distancia (ver la sección de mandos a distancia más abajo). 
<Refspec>

    Especifica los árbitros para ir a buscar, y que los árbitros locales para actualizar. Cuando no hay <refspec> s aparecerá en la línea de comandos, las referencias a buscar se leen de remote.<repository>.fetch variables en lugar (ver git-fetch [1] ).

    El formato de un parámetro <refspec> es un signo opcional de + , seguido por el árbitro fuente <src>, seguido de dos puntos : , seguido por el árbitro con destino <dst>. El colon se puede omitir cuando <dst> está vacía.

git stash:  Utilice git stash cuando se desea registrar el estado actual del directorio de trabajo y el índice, pero desea volver a un directorio de trabajo limpio. El comando guarda sus modificaciones locales de distancia y revierte el directorio de trabajo para que coincida con la HEAD cometió. 
Las modificaciones escondido lejos por este comando se pueden enumerar con git stash list , inspeccionados con git stash show , y restaurados (potencialmente en la parte superior de un diferente comprometerse) con git stash apply . Llamando git stash sin ningún argumento es equivalente al git stash save . Un escondite es por defecto aparece como "trabajo en curso sobre BRANCHNAME ...", pero se puede dar un mensaje más descriptivo en la línea de comandos cuando se crea uno. 
El último escondite que ha creado se almacena en refs/stash ; alijos de más edad se encuentran en el reflog de esta referencia y pueden nombrarse utilizando la sintaxis reflog habitual (por ejemplo stash@{0} es el alijo de más reciente creación, stash@{1} es el anterior, stash@{2.hours.ago} también es posible). 
Lista git alijo [<opciones>]
 git show de escondite [<alijo>]
 gota git alijo [-q | --quiet] [<alijo>]
 alijo git (pop | apliquen) [--index] [-q | --quiet] [<alijo>]
 alijo rama git <BRANCHNAME> [<alijo>]
 git alijo [guardar [-p | --patch] [-k | - [no-] keep-índice] [-q | --quiet]
	      [-u | --include-Untracked] [-a | --all] [<mensaje>]]
 alijo git clara
 git alijo crear [<mensaje>]
 git alijo tienda [-m | --message <mensaje>] [-q | --quiet] <cometer> 

OPCIONES

guardar [-p | --patch] [-k | - [no-] keep-índice] [-u | --include-untracked] [-a | --all] [-q | --quiet] [ <mensaje>]

    Guarde sus modificaciones locales a un nuevo escondite, y ejecutar git reset --hard para revertirlas. La <mensaje> parte es opcional y da la descripción junto con el estado guardado. Para hacer rápidamente una instantánea, se puede omitir tanto "salvar" y <mensaje>, pero dando sólo <mensaje> no activa esta acción para evitar un mal escrito subcomando de hacer un alijo no deseado.

    Si el --keep-index se usa la opción, todos los cambios ya se han agregado al índice se dejan intactos.

    Si el --include-untracked se utiliza la opción, todos los archivos sin seguimiento también se escondieron y luego limpiarse con git clean , dejando el directorio de trabajo en un estado muy limpio. Si el --all se usa la opción entonces los ficheros ignorados están escondidos y limpiados además de los archivos sin seguimiento.

    Con --patch , se puede seleccionar de forma interactiva trozos del diff entre la cabeza y el árbol de trabajo que se escondió. La entrada alijo está construido de tal manera que su estado índice es el mismo que el estado índice de su repositorio, y su worktree contiene sólo los cambios seleccionados de forma interactiva. Los cambios seleccionados se deshacen de su worktree. Vea la sección "Modo interactivo" de git-add [1] para aprender cómo operar el --patch modo.

    El --patch opción implica --keep-index . Puede usar --no-keep-index para anular esto. 
Lista [<opciones>]

    Enumerar los alijos que tiene actualmente. Cada alijo aparece con su nombre (por ejemplo stash@{0} es el último escondite, stash@{1} es la anterior, etc.), el nombre de la rama que estaba vigente cuando se hizo el escondite, y una breve Descripción de la comisión del alijo se basa en.

      alijo @ {0}: WIP en enviar: 6ebd0e2 ... Actualización de la documentación git-alijo
     alijo @ {1}: El maestro: 9cc0589 ... Añadir git-alijo 

    El comando tiene opciones aplicables al comando git log para controlar lo que se muestra y cómo. Ver git log [1] . 
mostrar [<alijo>]

    Mostrar los cambios registrados en el escondite como un diff entre el estado guardado y su principal original. Cuando no hay <stash> se da, muestra la más reciente. Por defecto, el comando muestra el diffstat, pero que aceptará cualquier formato conocido a git diff (por ejemplo, git stash show -p stash@{1} para ver el segundo alijo más reciente en forma de parche). Puede utilizar variables de configuración stash.showPatch stash.showStat y / o para cambiar el comportamiento por defecto. 
pop [--index] [-q | --quiet] [<alijo>]

    Retirar un solo estado escondido en la lista escondite y aplicarlo en la parte superior del estado del árbol de trabajo actual, es decir, hacer la operación inversa de git stash save . El directorio de trabajo debe coincidir con el índice.

    Aplicando el estado puede fallar con los conflictos; en este caso, no se elimina de la lista de escondite. Es necesario resolver los conflictos por la mano y la llamada git stash drop manualmente después.

    Si el --index se usa la opción, a continuación, intenta restablecer no sólo los cambios del árbol de trabajo, sino también los del índice. Sin embargo, esto puede fallar, cuando tiene conflictos (que se almacenan en el índice, en el que, por tanto, ya no se puede aplicar los cambios, ya que eran originalmente).

    Cuando no hay <stash> se da, stash@{0} se supone, de lo contrario <stash> debe ser una referencia de la forma stash@{<revision>} . 
aplicar [--index] [-q | --quiet] [<alijo>]

    Al igual que pop , pero no quite el estado de la lista alijo. A diferencia de pop , <stash> puede ser cualquier commit que se ve como una confirmación creado por stash save o stash create . 
rama <BRANCHNAME> [<alijo>]

    Crea y extrae una nueva rama llamada <branchname> a partir de la commit en el que el <stash> fue creada originalmente, aplica los cambios registrados en <stash> en el nuevo árbol de trabajo y el índice. Si que tiene éxito, y <stash> es una referencia de la forma stash@{<revision>} , entonces se deja caer el <stash> . Cuando no hay <stash> se da, se aplica la última.

    Esto es útil si la rama sobre la que se ha ejecutado git stash save ha cambiado lo suficiente que git stash apply falla debido a los conflictos. Desde el alijo se aplica en la parte superior de una confirmación de que era el jefe en el momento git stash se ejecute, se restablece el estado guardado originalmente sin conflictos. 
claro

    Retire todos los estados escondidos. Tenga en cuenta que esos estados entonces estará sujeto a la poda, y puede ser imposible recuperar (ver ejemplos a continuación para una posible estrategia). 
deje caer [-q | --quiet] [<alijo>]

    Retirar un solo estado guardado de la lista alijo. Cuando no hay <stash> se da, se elimina el más reciente. es decir stash@{0} , de lo contrario <stash> debe ser una referencia válida de registro alijo de la forma stash@{<revision>} . 
crear

    Crear un alijo (que es cometer un habitual objeto) y regresar su nombre de objeto, sin almacenarlo en cualquier parte del espacio de nombres ref. Este está destinado a ser útil para scripts. Probablemente no es el comando que desea utilizar; consulte "salvar" arriba. 
almacenar

    Almacenar un alijo dado creada a través de git alijo crear (que es una combinación de cometer colgando) en el que el árbitro escondite, la actualización de la reflog alijo. Este está destinado a ser útil para scripts. Probablemente no es el comando que desea utilizar; consulte "salvar" arriba.


EJEMPLOS

Entrando en un árbol sucia

    Cuando estás en el medio de algo, se entera de que hay cambios ascendentes que son posiblemente relevante para lo que está haciendo. Cuando los cambios locales no entren en conflicto con los cambios en la corriente arriba, un simple git pull le permitirá mover hacia adelante.

    Sin embargo, hay casos en los que los cambios locales entran en conflicto con los cambios ascendentes y git pull se niega a sobrescribir los cambios. En tal caso, se puede esconder sus cambios de distancia, lleve a cabo un tirón, y luego unstash, como esto:

      $ Git pull
      ...
     presentar foobar no hasta la fecha, no se puede fusionar.
     $ Git alijo
     $ Git pull
     $ Git alijo pop 

flujo de trabajo interrumpido

    Cuando estás en el medio de algo, su jefe entra y demandas que arreglar algo inmediatamente. Tradicionalmente, que haría una confirmación a una rama temporal para almacenar los cambios de distancia, y regresar a su sucursal original para hacer el arreglo de emergencia, así:

      # ... Hackear hackear hackear ...
     $ Git checkout -b my_wip
     $ Git commit -a -m "WIP"
     $ Git checkout master
     $ Corrección de edición de emergencia
     $ Git commit -a -m "Fix a toda prisa"
     $ Git checkout my_wip
     $ Git reset CABEZA --soft ^
     # ... Seguir la piratería ... 

    Puede utilizar alijo git para simplificar lo anterior, así:

      # ... Hackear hackear hackear ...
     $ Git alijo
     $ Corrección de edición de emergencia
     $ Git commit -a -m "Fix a toda prisa"
     $ Git alijo pop
     # ... Seguir la piratería ... 

Prueba de confirmaciones parciales

    Puede utilizar git stash save --keep-index cuando se quiere hacer dos o más commit de los cambios en el árbol de trabajo, y que desea probar cada cambio antes de comprometerse:

      # ... Hackear hackear hackear ...
     $ Git add --patch foo # añaden simplemente primera parte al índice
     $ Git alijo parada --keep-índice # guardar todos los otros cambios en el alijo
     $ Editar / construcción / prueba de primera parte
     $ Git commit -m '' Primera parte # comprometen cambio completamente probado
     $ git alijo pop # preparan para trabajar en todos los demás cambios
     # ... Repetir por encima de cinco pasos hasta que uno se comprometen restos ...
     $ Editar / construcción / prueba de las partes restantes
     $ Git commit -m 'foo' Las partes restantes


git stash pop: 
pop [--index] [-q | --quiet] [<alijo>] 
Retirar un solo estado escondido en la lista escondite y aplicarlo en la parte superior del estado del árbol de trabajo actual, es decir, hacer la operación inversa de git stash save . El directorio de trabajo debe coincidir con el índice. 
Aplicando el estado puede fallar con los conflictos; en este caso, no se elimina de la lista de escondite. Es necesario resolver los conflictos por la mano y la llamada git stash drop manualmente después. 
Si el --index se usa la opción, a continuación, intenta restablecer no sólo los cambios del árbol de trabajo, sino también los del índice. Sin embargo, esto puede fallar, cuando tiene conflictos (que se almacenan en el índice, en el que, por tanto, ya no se puede aplicar los cambios, ya que eran originalmente). 
Cuando no hay <stash> se da, stash@{0} se supone, de lo contrario <stash> debe ser una referencia de la forma stash@{<revision>} . 

git reset: En la primera y segunda forma, copiar entradas de <tree-ish> para el índice. En la tercera forma, establecer la rama actual cabeza (cabeza) a <cometer>, modificando opcionalmente el índice y el árbol para que coincida trabajo. La <tree-ish> / <cometer> incumplimientos a la cabeza en todas las formas. 
git reset [q] [<-ish árbol>] [-] <> caminos ... 
Esta forma restablece las entradas de índice para todos los caminos <> a su estado a <árbol-ish>. (No afecta el árbol de trabajo o de la rama actual.) 
Esto significa que git reset <paths> es lo contrario de git add <paths> . 
Después de ejecutar git reset <paths> para actualizar la entrada de índice, puede utilizar git-checkout [1] para comprobar el contenido del índice para el árbol de trabajo. Por otra parte, el uso de git-checkout [1] y especificando una confirmación, puede copiar el contenido de un camino para salir de un envío al índice y al árbol de trabajo de una sola vez. 
git reset (--patch | -p) [<ish-árbol>] [-] [<caminos> ...] 
Interactivamente seleccionar trozos en la diferencia entre el índice y <ish-árbol> (por defecto a la cabeza). Los trozos elegidos se aplican a la inversa para el índice. 
Esto significa que git reset -p es lo contrario de git add -p , es decir, que se puede utilizar para reiniciar selectivamente trozos. Vea la sección "Modo interactivo" de git-add [1] para aprender cómo operar el --patch modo. 
git reset [<modo>] [<cometer>] 
Esta forma se restablece la cabeza rama actual a <cometer> y posiblemente actualiza el índice (que se quede en el árbol de la <cometer>) y el árbol de trabajo en función de <modo>. Si se omite <modo>, por defecto es "--mixed". La <modo> debe ser uno de los siguientes: 
--suave 
No toca el archivo de índice o el árbol de trabajo en absoluto (pero restablece la cabeza a <comprometen>, al igual que todos los modos de hacer). Esto deja a todos sus archivos modificados "Los cambios que se cometan", como git status lo pondría. 
--mezclado 
Restablece el índice, pero no el árbol de trabajo (es decir, los archivos modificados se conservan pero no marcados para cometer) e informa de lo que no se ha actualizado. Esta es la acción por defecto. 
Si -N se especifica, las rutas eliminadas se marcan como por intención de sumar (ver git-add [1] ). 
--difícil 
Restablece el índice y el árbol de trabajo. Cualquier cambio en los archivos rastreados en el árbol de trabajo desde comprometerse <> se descartan. 
--unir 
Restablece el índice y actualiza los archivos en el directorio de trabajo que son diferentes entre <cometer> y la cabeza, pero mantiene los cuales son diferentes entre el índice y el árbol de trabajo (es decir, que tiene cambios que no se han añadido). Si un archivo que es diferente entre <cometer> y el índice tiene cambios unstaged, reinicio se aborta. 
En otras palabras, --merge hace algo como un git lectura árbol -u -m <cometer>, pero lleva entradas de índice hacia adelante sin combinar. 
--guardar 
Restablece las entradas de índice y actualiza los archivos en el directorio de trabajo que son diferentes entre <cometer> y la cabeza. Si un archivo que es diferente entre <cometer> y HEAD tiene cambios locales, reinicio se aborta. 
Si desea deshacer un compromiso que no sea la última en una rama, git-revertir [1] es su amigo. 
git reset [q] [<-ish árbol>] [-] <> caminos ...
git reset (--patch | -p) [<ish-árbol>] [-] [<caminos> ...]
git reset [--soft |  --mixed [N] |  --hard |  --merge |  --keep] [q] [<cometer>] 

OPCIONES

-q
--tranquilo

    Sé tranquila, a sólo reportar errores. 

EJEMPLOS

Deshacer añadir

      $ Editar (1)
     $ Git add filfre.c frotz.c
     $ Mailx (2)
     Reinicio $ git (3)
     $ Git tirón: nitfol //info.example.com/ (4) 

        Usted está trabajando felizmente en algo, y encontrar los cambios en estos archivos están en buen estado. Usted no quiere verlos cuando se ejecuta "git diff", porque va a trabajar en otros archivos y cambios con estos archivos son una distracción.

        Alguien le pide que tira de él, y los cambios de sonidos dignos de fusión.

        Sin embargo, ya se ha ensuciado el índice (es decir, el índice no coincide con la CABEZA cometer). Pero sabes el tirón que va a hacer que no afecta frotz.c o filfre.c, por lo que revierte los cambios del índice para estos dos archivos. Los cambios en árbol de trabajo permanecen allí.

        A continuación, puede tirar y fusionarse, dejando a los cambios frotz.c y filfre.c todavía en el árbol de trabajo. 

Deshacer y rehacer una confirmación

      $ Git commit ...
     $ Git reset CABEZA --soft ^ (1)
     $ Editar (2)
     $ Git commit -a ORIG_HEAD -c (3) 

        Esto se realiza con mayor frecuencia cuando se acordó de lo que acaba de cometer es incompleta, o mal escrito sus mensajes de cambios, o ambos. Deja el árbol de trabajo como lo era antes "reset".

        Realizar correcciones en los archivos del árbol de trabajo.

        "Reset" copia la vieja cabeza de .git / ORIG_HEAD; rehacer el envío de datos, comenzando con su mensaje de registro. Si no necesita editar el mensaje más allá, se puede dar la opción -C lugar. 

    Ver también la opción --amend a git-commit [1] . 
Deshacer un compromiso, por lo que es una rama tema

      $ Git branch tema / WIP (1)
     $ Git reset CABEZA --hard ~ 3 (2)
     $ Git checkout tema / WIP (3) 

        Usted ha hecho algunas confirmaciones, pero se dan cuenta que fueron prematuros estar en la rama "master". Desea continuar el pulido en una rama puntual, por tanto, crear rama "tema / WIP" fuera de la CABEZA actual.

        Rebobinar la rama principal para deshacerse de esas tres confirmaciones.

        Cambiar a la rama "tema / WIP" y seguir trabajando. 

Deshacer compromete de forma permanente

      $ Git commit ...
     $ Git reset CABEZA --hard ~ 3 (1) 

        Los últimos tres commit (cabeza, cabeza del ^, y la cabeza ~ 2) eran malos y que no quieren a ver más. No haga esto si ya ha dado a estos commit en otra persona. (Vea la sección "Recuperación desde aguas arriba REBASE" en git-rebase [1] de las consecuencias de su acción.) 

Deshacer una fusión o tirar

      Tirón $ git (1)
     Auto-fusión nitfol
     CONFLICTO (contenido): Combinar conflicto en nitfol
     fusión automática falló;  solucionar conflictos y luego confirmar el resultado.
     $ Git reset --hard (2)
     $ Git pull.  tema / rama (3)
     Actualización a partir de 41223 ... 13134 ... a
     Avance rápido
     $ Git reset ORIG_HEAD --hard (4) 

        Trate de actualizar desde la corriente arriba dio lugar a una gran cantidad de conflictos; usted no estaba dispuesto a pasar mucho tiempo fusionando en este momento, por lo que decide hacerlo más adelante.

        "Pull" no ha hecho cometer fusión, por lo que "git restablecer --hard", que es sinónimo de "git reset CABEZA --hard" limpia el desorden del archivo de índice y el árbol de trabajo.

        Fusionar una rama tema en la rama actual, lo que resultó en un avance rápido.

        Sin embargo, se decidió que la rama puntual no está lista para el consumo público todavía. "Pull" o "fusionar" siempre deja la punta original de la rama actual en ORIG_HEAD, así restablecer difícil que trae el archivo de índice y el árbol de trabajo de nuevo a ese estado, y restablece la punta de la rama a la que se comprometen. 

Deshacer una fusión o tirar dentro de un árbol de trabajo sucia

      Tirón $ git (1)
     Auto-fusión nitfol
     Fusionar adoptada por recursiva.
      nitfol |  20 +++++ ----
      ...
     $ Git reset ORIG_HEAD --merge (2) 

        Incluso si usted puede tener modificaciones locales en su árbol de trabajo, se puede decir con seguridad "git pull" cuando se sabe que el cambio en la otra rama no se superpone con ellos.

        Después de inspeccionar el resultado de la fusión, es posible que el cambio en la otra rama es insatisfactoria. Running "git reset ORIG_HEAD --hard" le permitirá volver a donde estabas, pero va a descartar los cambios locales, que usted no quiere. "Git reset --merge" mantiene sus cambios locales. 

flujo de trabajo interrumpido

    Suponga que se recibe una solicitud de corrección de urgencia cuando esté en medio de un gran cambio. Los archivos en su árbol de trabajo no están en forma para estar comprometido todavía, pero hay que llegar a la otra rama de corrección de errores rápida.

      función $ git checkout; # que estaba trabajando en la rama "característica" y
     $ Trabajo trabajo trabajo; # quedó interrumpido
     $ Git commit -a -m "instantánea WIP" (1)
     $ Git checkout master
     $ Fix fix fix
     $ Git commit; # comprometen con el registro de bienes
     característica git checkout $
     $ Git reset CABEZA --soft ^; # volver al estado WIP (2)
     Reinicio $ git (3) 

        Esto se cometen se vuelen por lo que un mensaje de registro de usar y tirar está bien.

        Esto elimina el trabajo en curso de la historia cometer cometer, y establece su árbol de trabajo para el estado justo antes de hacer esa instantánea.

        En este punto, el archivo de índice todavía tiene todo cambia el trabajo en curso que se cometan como WIP instantánea. Esto actualiza el índice para mostrar sus archivos de trabajo en curso como no comprometida. 

    Ver también git-alijo [1] . 
Restablecer un único archivo en el índice

    Supongamos que haya agregado un archivo en el índice, pero después decide que no desea añadirlo a su confirmación. Se puede eliminar el archivo de índice, manteniendo sus cambios con git reset.

      Reinicio $ git - frotz.c (1)
     $ Git commit -m "Commit archivos de índice" (2)
     $ Git add frotz.c (3) 

        Esto elimina el archivo del índice mientras lo mantiene en el directorio de trabajo.

        Esto compromete a todos los demás cambios en el índice.

        Agrega el archivo al índice de nuevo. 

Guarde los cambios en el árbol de trabajo mientras se descartan algunas confirmaciones sobre las previas

    Suponga que está trabajando en algo y comprometerse, y luego continúa trabajando un poco más, pero ahora usted piensa que lo que tiene en su árbol de trabajo debe estar en otra rama que no tiene nada que ver con lo que usted ha cometido con anterioridad. Puede iniciar una nueva rama y restablecerla, manteniendo los cambios en su árbol de trabajo.

      $ Git tag inicio
     $ Git checkout -b BRANCH1
     $ editar
     $ Git commit ... (1)
     $ editar
     $ Git checkout -b BRANCH2 (2)
     Reinicio $ git --keep empezar (3) 

        Todo ello lleva a sus primeras ediciones en BRANCH1.

        En el mundo ideal, que podría haber dado cuenta de que cuanto más temprano se comprometan no pertenecen al nuevo tema cuando se creó y se cambió a BRANCH2 (es decir, "git checkout -b BRANCH2 start"), pero nadie es perfecto.

        Pero se puede utilizar "reset --keep" para eliminar cometer el no deseado después de cambiar al "BRANCH2".
git cherry-pick
 
https://librosweb.es/libro/pro_git/

Computación en la nube
1)	 Investigar.
a.	¿Qué significan las siglas IaaS, PaaS, y SaaS? Explique las diferencias con ejemplos practicos.
Software-as-a-Service (SaaS): El concepto de SaaS ha existido desde hace mucho tiempo, pero quizás en estos últimos años hemos definido claramente a que nos referimos. Básicamente se trata de cualquier servicio basado en la web. Tenemos ejemplos claros como el Webmail de Gmail, los CRM onlines. En este tipo de servicios nosotros accedemos normalmente a través del navegador sin atender al software. Todo el desarrollo, mantenimiento, actualizaciones, copias de seguridad es responsabilidad del proveedor.

En este caso tenemos poco control, nosotros nos situamos en la parte más arriba de la capa del servicio. Si el servicio se cae es responsabilidad de proveedor hacer que vuelva a funcionar.

Ejemplos populares de Saas son Google Docs, Salesforce, Dropbox, Gmail…

Plataform-as-a-Service (PaaS): PaaS es el punto donde los desarrolladores empezamos a tocar y desarrollar nuestras propias aplicaciones que se ejecutan en la nube. En este caso nuestra única preocupación es la construcción de nuestra aplicación, ya que la infraestructura nos la da la plataforma.

Es un modelo que reduce bastante la complejidad a la hora de desplegar y mantener aplicaciones ya que las soluciones PaaS gestionan automáticamente la escalabilidad usando más recursos si fuera necesario. Los desarrolladores aun así tienen que preocuparse de que sus aplicaciones estén lo mejor optimizadas posibles para consumir menos recursos posibles (número de peticiones, escrituras en disco, espacio requerido, tiempo de proceso, etc..) Pero todo ello sin entrar al nivel de maquinas.

Ejemplos populares son Google App Engine que permite desarrollar aplicaciones en Java o Python desplegándolas en la infraestructura que provee Google, cosa que también hace Heroku con Rails y Django.

Para los desarrolladores que ignoran la infraestructura que deben montar y sólo quieren preocuparse de escribir software, esta es la alternativa a seguir.

Infraestructure-as-a-Service (IaaS):  En este caso con IaaS tendremos mucho más control que con PaaS, aunque a cambio de eso tendremos que encargarnos de la gestión de infraestructura,

El ejemplo perfecto es el proporcionado por Amazon Web Service (AWS) que no provee una serie de servicios como EC2 que nos permite manejar maquinas virtuales en la nube o S3 para usar como almacenamiento. Nosotros podemos elegir qué tipo de instancias queremos usar LInux o Windows, así como la capacidad de memoria o procesador de cada una de nuestras maquinas. El hardware para nosotros es transparente, todo lo que manejamos es de forma virtual.

La principal diferencia es que nosotros nos encargamos de escalar nuestras aplicaciones según nuestras necesidades, además de preparar todo el entorno en las maquinas (aunque existen imágenes de instancias preparadas con las configuraciones más comunes).

Además de AWS nos encontramos ejemplos como Rackspace Cloud o vCloud de VMWare.

http://www.genbetadev.com/programacion-en-la-nube/entendiendo-la-nube-el-significado-de-saas-paas-y-iaas

b.	¿Qué es Heroku?

Heroku es una plataforma en la nube que permite a las empresas a construir, entregar, supervisar y aplicaciones escala; es la manera más rápida para ir de la idea al URL, sin pasar por todos esos problemas de infraestructura.

Heroku desarrollada desde junio de 2007, con el objetivo de soportar el lenguaje de programación Ruby, pero después se ha extendido el soporte a Java, Node.js, Scala, Clojure y Python y PHP. La base del sistema operativo es Debian.

James Lindenbaum, Adam Wiggins, y Orion Henry fundaron Heroku. El 8 de diciembre de 2010 Salesforce.com adquirió Heroku como una subsidiaria. El 12 de julio de 2011 Yukihiro “Matz” Matsumoto, el creador de Ruby se unió a la empresa. Ese mismo mes, Heroku incorporó el soporte para Node.js y Clojure.

Actualmente Heroku soporta Cloudant, Couchbase Server, MongoDB y Redis,6 además de la conocida PostgreSQL.

En Heroku tenemos que conocer algo llamado Dynos. Los Dynos son piezas fundamentales del modelo de arquitectura de Heroku, son las unidades que proveen capacidad de cómputo dentro de la plataforma. Están basados en Contenedores Linux.

Cada Dyno está aislado del resto, por lo que los comandos que se ejecutan y los archivos que se almacenan en un Dyno, no afectan a los otros. Además cada Dyno provee el ambiente requerido por las aplicaciones para ser ejecutadas.

Los posibles comandos a ser ejecutados en los dynos incluyen procesos web, o cualquier otro tipo de proceso definido en el archivo Procfile de la aplicación. Este es un archivo de texto ubicado en el directorio raíz de la aplicación, y es el mecanismo provisto para la declaración de comandos que luego correrán los dynos. Básicamente, consiste de una lista de tipos de procesos de la aplicación. Cada tipo de procesos constituye una declaración de un comando.
Principales características

    Elasticidad y crecimiento. La cantidad de Dynos asignados a una aplicación se puede cambiar en cualquier momento a través de la línea de comandos o el dashboard.

    Tamaño. Heroku ofrece diferentes tipos de dynos, cada uno con diferentes capacidades de procesamiento y memoria.

    Routing. Internamente los routers realizan un seguimiento de la ubicación de los Dynos que estén corriendo, y redirigen el tráfico de acuerdo a la misma.

    Seguimiento. Existe un manejador de Dynos, el cual monitorea de forma continua los dynos que se estén ejecutando. En caso de una falla en un Dyno, este es eliminado y creado nuevamente.

    Distribución y redundancia. Los Dynos se encuentran aislados uno de otro. Esto implica que de existir fallos en la infraestructura interna de alguno de ellos, los otros dynos no se ven afectados, y consecuentemente tampoco la aplicación.

http://kawcode.com/tutoriales/que-es-heroku/

2)	Registrarse en la plataforma de Heroku y descargar Heroku Toolbet para desarrollar aplicaciones.
 
Herramientas de Software
3)	¿Qué es Node.js?
Node.js es una librería y entorno de ejecución de E/S dirigida por eventos y por lo tanto asíncrona que se ejecuta sobre el intérprete de JavaScript creado por Google V8. Lo cierto es que está muy de moda aunque no es algo nuevo puesto que existen librerías como Twisted que hacen exactamente lo mismo pero si es cierto que es la primera basada en JavaScript y que tiene un gran rendimiento.

¿Cuál es su importancia hoy?,
Node.js es un entorno Javascript del lado del servidor, basado en eventos. Node ejecuta javascript utilizando el motor V8, desarrollado por Google para uso de su navegador Chrome. Aprovechando el motor V8 permite a Node proporciona un entorno de ejecución del lado del servidor que compila y ejecuta javascript a velocidades increíbles. El aumento de velocidad es importante debido a que V8 compila Javascript en código de máquina nativo, en lugar de interpretarlo o ejecutarlo como bytecode. Node es de código abierto, y se ejecuta en Mac OS X, Windows y Linux.

¿Por qué muchas empresas en mundo usan Node.js?
Con Node.js las empresas están a la vanguardia tecnológica, se mantienen competitivas con respecto a las soluciones que ofrecen y alivian un poco el problema de reclutar talento.

4)	¿Qué es EXPRESSJS? De otros ejemplos
Es un framework de desarrollo de aplicaciones web minimalista y flexible para Node.js". Está inspirado en Sinatra, además es robusto, rápido, flexible y muy simple. Entre otras características, ofrece Router de URL (Get, Post, Put …), facilidades para motores de plantillas (Jade, EJS, JinJS …), Middeleware via Connect y un buen test coverage

Usage: express [options] [path]
 
Options:
  -s, --sessions           add session support
  -t, --template <engine>  add template <engine> support (jade|ejs). default=jade
  -c, --css <engine>       add stylesheet <engine> support (stylus). default=plain css
  -v, --version            output framework version
  -h, --help               output help information

5)	¿Qué son los WebSockets?
es una tecnología avanzada que hace posible abrir una sesión de comunicación interactiva entre el navegador del usuario y un servidor. Con esta  API, puede enviar mensajes a un servidor y  recibir  respuestas controladas por eventos sin tener que consultar al servidor para una respuesta.
¿Que es Socket.IO?
Socket.io es una librería que nos permite manejar eventos en tiempo real mediante una conexión TCP y todo ello en JavaScript. Es realmente potente y podemos hacer todo tipo de aplicaciones en tiempo real
http://www.nodehispano.com/2012/09/introduccion-a-socket-io-nodejs/
Social media 	
6)	Investigar
a.	¿Qué es Twitter Streaming API? 
as API de Streaming dan a los desarrolladores acceso de baja latencia a la corriente mundial de Twitter Tweet de los datos. Una aplicación adecuada de un cliente de streaming será empujado mensajes que indican los Tweets y se han producido otros hechos, sin ninguna de la sobrecarga asociada a un sondeo extremo REST.
Dar un ejemplo de su uso en productos comerciales o por parte de alguna empresa.
Por ejemplo, considere una aplicación web que acepta peticiones de los usuarios, hace una o más peticiones a la API de Twitter, a continuación, formatos e imprime el resultado al usuario, como una respuesta a la petición inicial del usuario: 
 
Una aplicación que se conecta a la Transmisión de API no será capaz de establecer una conexión en respuesta a una solicitud del usuario, como se muestra en el ejemplo anterior. En su lugar, el código para el mantenimiento de la conexión de transmisión normalmente se ejecuta en un proceso independiente del proceso que trata las solicitudes HTTP: 
 
El proceso de transmisión obtiene los Tweets de entrada y lleva a cabo cualquier análisis, el filtrado, y / o agregación necesaria antes de guardar el resultado a un almacén de datos. El proceso de manipulación de HTTP consulta el almacén de datos de resultados en respuesta a peticiones de los usuarios. Si bien este modelo es más complejo que el primer ejemplo, los beneficios de tener un flujo en tiempo real de los datos Tweet hacen que la integración de mérito para muchos tipos de aplicaciones. 
https://dev.twitter.com/streaming/overview

