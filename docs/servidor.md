# Monta tu propio servidor

Esta guía crea un mundo propio de Mineclonia. No replica el Castillo, sus archivos ni la configuración privada del proyecto.

## 1. Ensayo en LAN

1. Instala [Luanti](https://www.luanti.org/en/downloads/) en el equipo que hará de anfitrión y en el equipo de un jugador.
2. En el anfitrión, instala Mineclonia desde el navegador de contenido y crea un mundo de prueba. En el menú principal activa **Host Server** (o su equivalente traducido), define el usuario del anfitrión y su contraseña, y levanta el mundo.
3. Desde el segundo equipo, en la misma red local, abre **Unirse a un juego** y usa la dirección local del anfitrión y el puerto configurado. Luanti usa **UDP**, habitualmente `30000`. No necesitas reenvío en el router para este ensayo.
4. Coloca un bloque de prueba, cierra el servidor correctamente y comprueba que el bloque sigue ahí después de iniciarlo de nuevo.

## 2. Servidor dedicado

1. Elige el método correspondiente a tu sistema en la [guía oficial de servidores](https://docs.luanti.org/for-server-hosts/setup/). El arranque dedicado no depende de que el cliente de escritorio siga abierto.
2. Instala Mineclonia en la carpeta de juegos de la instancia dedicada y crea un mundo asociado. Si usas contenedor, persiste el almacenamiento del mundo y la configuración fuera del contenedor; anota las versiones del motor, juego y mods.
3. Mantén la instancia fuera del directorio público, por ejemplo con `server_announce = false`. Eso evita anunciarla, pero **no restringe el acceso**: haz el primer ensayo en LAN, mantén el tráfico limitado a la red autorizada y usa controles de acceso si permites conexiones externas.
4. Agrega mods compatibles de uno en uno. Haz un respaldo antes de actualizar y comprueba una restauración en otra carpeta antes de depender de él.

### Si algo no conecta

- **No hay respuesta:** verifica que el servidor esté iniciado; comprueba puerto UDP, dirección y firewall.
- **Error de versión:** usa una combinación cliente/servidor compatible y confirma los requisitos de Mineclonia.
- **Bloques desconocidos al restaurar:** verifica que el respaldo y la instancia de prueba incluyan el mismo juego y mods antes de tocar el mundo original.

[Guía para jugadores](jugar.md) · [Volver al inicio](../README.md)
