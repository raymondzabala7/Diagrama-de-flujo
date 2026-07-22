Caso de estudio: "NovaPlay Studios"

Contexto: NovaPlay Studios es una empresa que desarrolla y distribuye videojuegos digitales. Necesita una base de datos para gestionar sus juegos, los estudios que los desarrollan, las plataformas donde están disponibles, los jugadores registrados, sus compras y los logros que desbloquean dentro de cada juego.

Requisitos del negocio:

Cada juego es desarrollado por un estudio (desarrollador), y un estudio puede desarrollar muchos juegos.
Un juego puede estar disponible en varias plataformas (PC, PS5, Xbox, etc.), y una plataforma aloja muchos juegos → relación N:M.
Los jugadores se registran en la plataforma y pueden comprar varios juegos; cada juego puede ser comprado por muchos jugadores → relación N:M, con atributos propios como fecha y monto.
Cada juego define sus propios logros (achievements); un logro pertenece a un único juego.
Un jugador puede desbloquear muchos logros, y un logro puede ser desbloqueado por muchos jugadores → N:M.
Un jugador puede tener, opcionalmente, una cuenta premium (beneficios extra) → relación 1:1.

Con estos requisitos identificamos las entidades fuertes (Desarrolladores, Videojuegos, Plataformas, Jugadores, Logros) y las entidades asociativas que resuelven las relaciones N:M y que además guardan sus propios atributos (Compras, Juego_Plataforma, Jugador_Logro).

Entidades fuertes: DESARROLLADORES, VIDEOJUEGOS, PLATAFORMAS, JUGADORES, LOGROS — cada una tiene su propia llave primaria (PK) independiente.
Entidades asociativas (resuelven las relaciones N:M y guardan datos propios):
JUEGO_PLATAFORMA → resuelve "un juego en varias plataformas".
COMPRAS → resuelve "un jugador compra varios juegos", guardando fecha y monto.
JUGADOR_LOGRO → resuelve "un jugador desbloquea varios logros", guardando fecha_obtenido.
Relación 1:1: JUGADORES – CUENTA_PREMIUM, opcional (no todo jugador tiene cuenta premium).
Relaciones 1:N: DESARROLLADORES → VIDEOJUEGOS, y VIDEOJUEGOS → LOGROS.

Promt:
Creame un caso de estudio para una empresa de videojuegos y crea un MER
