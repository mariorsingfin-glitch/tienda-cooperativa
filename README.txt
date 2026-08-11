CRENERGÍA V9 — IDENTIDAD VISUAL

Cambios:
- CRENERGÍA pasa a ser la identidad visual de la plataforma general.
- Se incorpora el nuevo símbolo minimalista de la App.
- Tienda Cooperativa identifica el módulo comercial / generación solar.
- Se utiliza la imagen visual de cotizaciones como fondo, con tratamiento oscuro.
- El icono PWA de Android / pantalla principal usa el nuevo símbolo de CRENERGÍA.
- Se mantiene el acceso por roles y la lógica funcional de la versión 8.

CLAVES DE DEMOSTRACIÓN:
Cliente: CLIENTE2026
Asesor: ASESOR2026
Ingeniería: ING2026
Administrador: ADMIN2026
Gerencia: GERENCIA2026

PUBLICACIÓN:
1. Descomprima el ZIP.
2. Suba/reemplace TODOS los archivos y la carpeta assets en la raíz del repositorio.
3. Commit en main.
4. Espere despliegue verde.
5. Abra por primera vez con ?v=9.

IMPORTANTE:
No olvide subir la carpeta assets. Si falta, los logotipos y el fondo no aparecerán.


V10 - PERSISTENCIA LOCAL
Los valores del Administrador ahora quedan guardados en localStorage y permanecen
después de recargar o cerrar la aplicación en el mismo navegador/dispositivo.

Importante: no se comparten con otros dispositivos o usuarios. Para eso hace falta
una base de datos/backend común.


V10.1 — CÓDIGO FIJO
- Se incorpora el Código Fijo como identificador del suministro/predio.
- Se solicita durante el asistente del cliente.
- Se precarga automáticamente en el simulador.
- Se guarda localmente junto con la última simulación.
- Está preparado conceptualmente para enlazar con una base central y precargar:
  ubicación, categoría tarifaria, consumo histórico y otros datos disponibles del suministro.


V11 — ETAPA 1 SUPABASE
- technical_parameters y tariffs se leen desde Supabase al iniciar.
- Supabase es la fuente maestra de esos dos grupos.
- Si Supabase no responde, se usa el último respaldo local.
- La App muestra “Base central conectada” cuando la lectura funciona.
- Costos, financiamiento y reglas comerciales siguen siendo locales.
- Las ediciones de parámetros técnicos y tarifas desde Administrador son temporales/locales.
- La escritura central queda pendiente de Supabase Auth + RLS de UPDATE.
