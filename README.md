# Accesos Vasculares — Hospital del Salvador

> Guía clínica rápida sobre dispositivos de acceso vascular para personal de enfermería y medicina.

---

## ¿Qué es esto?

Aplicación web de referencia clínica diseñada para el equipo del **Hospital del Salvador**. Permite consultar rápidamente los distintos dispositivos de acceso vascular —PICC, CVC, Midline y catéteres periféricos— incluyendo indicaciones, anatomía de inserción, longitudes, calibres y consideraciones de seguridad.

El objetivo es servir como apoyo visual durante la práctica clínica diaria, con información precisa y accesible desde cualquier dispositivo.

---

## Dispositivos cubiertos

| Dispositivo | Tipo | Posición de punta |
|---|---|---|
| **PICC** | Central | VCS / Unión cavoatrial |
| **CVC** | Central | Vena cava superior |
| **Midline** | Periférico largo | Vena axilar |
| **Catéter periférico** | Periférico | Vena antecubital / dorsal |

---

## Stack tecnológico

- **[Astro 6](https://astro.build/)** — framework principal, renderizado estático
- **[React 19](https://react.dev/)** — componentes interactivos
- **[Tailwind CSS 4](https://tailwindcss.com/)** — estilos utilitarios
- **[GSAP 3](https://gsap.com/)** — animaciones de entrada y scroll
- **[Vercel](https://vercel.com/)** — hosting y analytics

---

## Estructura del proyecto

```
src/
├── layouts/
│   └── BaseLayout.astro      # Layout base, header, navegación
├── pages/
│   └── index.astro           # Página principal (hero, secciones)
├── components/
│   ├── BentoGrid.astro       # Cuadrícula editorial de dispositivos
│   ├── DeviceSelector.astro  # Selector interactivo de dispositivos
│   ├── VascularMap.astro     # Mapa anatómico vascular
│   └── ...
└── styles/
    └── global.css            # Variables CSS, tipografía, tokens
```

---

## Desarrollo local

**Requisitos:** Node.js 18+

```bash
# Instalar dependencias
npm install

# Servidor de desarrollo (http://localhost:4321)
npm run dev

# Build de producción
npm run build

# Preview del build
npm run preview
```

---

## Deploy

El proyecto se despliega automáticamente en **Vercel** al hacer push a `main`.

```bash
# Build command
npm run build

# Output directory
dist/
```

---

## Diseño

La interfaz sigue una estética editorial oscura con tipografía serif (**DM Serif Display**) para los títulos y **Plus Jakarta Sans** para el cuerpo. La paleta usa un fondo casi negro (`#080b13`) con acentos en dorado (`#D4A853`) y esmeralda (`#34D399`).

La cuadrícula principal es un **Bento Grid asimétrico** de 3 columnas donde cada tarjeta expone los datos clínicos clave del dispositivo de forma escaneable.
