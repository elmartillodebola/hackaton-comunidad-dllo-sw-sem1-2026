# BuildDay Fintech Edition
### Comunidad Desarrollo de Software · Protección S.A.

Página web con el diseño y documentación del Ejercicio Práctico **BuildDay Fintech Edition**, organizado por la Comunidad de Desarrollo de Software de Protección S.A.

---

## Contenido

La página cubre toda la información del ejercicio:

- **Filosofía** — Por qué este formato y sus principios
- **5 Retos candidatos** — Con variantes por nivel (Iniciando, Junior, Senior, Mentor)
- **Votación en vivo** — Cómo se elige el reto el día de apertura
- **Articulación de equipos** — Composición y rol del Dev ancla/Dev CIS
- **Entregables** — Qué debe presentar cada equipo
- **Criterios de evaluación** — Puntos base y bonus
- **Estructura de la semana** — Del 8 al 15 de abril
- **Reglas** — Las normas del juego

---

## Estructura del proyecto

```
├── index.html              # Página principal (versión con identidad de marca)
├── hackathon-design.html   # Versión original (tema oscuro)
├── assets/
│   ├── BannerComunidadDlloSw.png       # Banner Comunidad Desarrollo de Software
│   ├── LogoIndividualCommDlloSW.png    # Ícono logo comunidad
│   └── NuevoLogoProteccionSura.jpg     # Logo Protección S.A.
├── .gitlab-ci.yml          # Pipeline de despliegue automático
└── README.md
```

---

## Tecnología

Página estática en HTML/CSS puro — sin dependencias ni frameworks externos.

- Fuente: [Sura](https://fonts.google.com/specimen/Sura) vía Google Fonts
- Colores: paleta oficial Comunidad Desarrollo de Software
- Compatible con cualquier navegador moderno

---

## Despliegue

Publicada vía **GitLab Pages**. El pipeline de CI/CD definido en `.gitlab-ci.yml` despliega automáticamente con cada push a `main`.

```yaml
pages:
  stage: deploy
  script:
    - mkdir -p public
    - cp index.html public/
    - cp -r assets public/
  artifacts:
    paths:
      - public
  only:
    - main
```

---

## Fechas clave

| Fecha | Hito |
|---|---|
| Semana previa al 8 de abril | Publicación de los 5 retos y votación previa |
| Martes 8 de abril · 8:00 am | Sesión de apertura y votación en vivo |
| Jueves 10 de abril · 8:00 am | Checkpoint intermedio |
| Lunes 14 de abril · 11:59 pm | Freeze de código |
| Martes 15 de abril · 8:00 am | Demos y cierre |

---

*Comunidad Desarrollo de Software · Protección S.A.*
