# IAn Groove — web oficial

Web estática construida con Astro. Las canciones se actualizan desde un único archivo y el resultado se puede publicar gratuitamente con GitHub y Cloudflare Pages.

## Ver la web en local

```bash
pnpm install
pnpm dev
```

Astro mostrará una dirección local, normalmente `http://localhost:4321`.

## Añadir un lanzamiento

1. Copia la portada original a `src/assets/covers/`. Astro creará automáticamente versiones WebP más ligeras.
2. Abre `src/data/songs.json`.
3. Duplica una canción existente y cambia título, portada, descripción y fecha.
4. Añade únicamente enlaces públicos comprobados dentro de `links`.
5. Marca solo el lanzamiento más reciente con `"featured": true` y cambia el anterior a `false`.
6. Ejecuta `pnpm build` antes de publicar.

Si una plataforma no tiene enlace real, no la añadas: la web no mostrará ese botón.

## Publicar con GitHub y Cloudflare Pages

1. Crea un repositorio de GitHub y sube esta carpeta.
2. En Cloudflare Pages elige **Conectar con Git** y selecciona el repositorio.
3. Configura **Astro** como framework.
4. Usa `pnpm build` como comando de compilación y `dist` como carpeta de salida.
5. Guarda y despliega. Los siguientes cambios se publicarán automáticamente al subirlos a GitHub.

La web usa Node 20, indicado en `.node-version`.
