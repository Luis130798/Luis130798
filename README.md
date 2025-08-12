<!-- ==========================
     README - Ing. José Luis Apaza Quispe
     Estilo: Corporativo / Futurista / Serio
     ========================== -->

<!-- Header: SVG logo + Title -->
<p align="center">
  <!-- Inline SVG: sobrio, animado (ondas RF) -->
  <svg xmlns="http://www.w3.org/2000/svg" width="820" height="160" viewBox="0 0 820 160" preserveAspectRatio="xMidYMid meet">
    <defs>
      <linearGradient id="g1" x1="0" x2="1">
        <stop offset="0" stop-color="#0ff" stop-opacity="0.95"/>
        <stop offset="1" stop-color="#00a" stop-opacity="0.95"/>
      </linearGradient>
      <filter id="f1" x="-50%" y="-50%" width="200%" height="200%">
        <feGaussianBlur stdDeviation="6" result="b"/>
        <feBlend in="SourceGraphic" in2="b"/>
      </filter>
    </defs>

    <!-- background -->
    <rect width="820" height="160" rx="12" fill="#071019"/>

    <!-- logo: antenna + waves -->
    <g transform="translate(32,24)">
      <g transform="scale(1)">
        <rect x="0" y="0" width="112" height="112" rx="12" fill="#06121a"/>
        <path d="M56 24 L64 48 L48 48 Z" fill="#00ffd0" opacity="0.95"/>
        <rect x="52" y="48" width="8" height="36" rx="2" fill="#00ffd0"/>
        <!-- concentric waves animated (SMIL) -->
        <g fill="none" stroke="url(#g1)" stroke-width="1.6" stroke-opacity="0.9">
          <circle cx="56" cy="44" r="20">
            <animate attributeName="r" values="20;34;20" dur="3.6s" repeatCount="indefinite"/>
            <animate attributeName="stroke-opacity" values="0.35;0.85;0.35" dur="3.6s" repeatCount="indefinite"/>
          </circle>
          <circle cx="56" cy="44" r="36" stroke-width="1.1">
            <animate attributeName="r" values="36;54;36" dur="3.6s" begin="0.6s" repeatCount="indefinite"/>
            <animate attributeName="stroke-opacity" values="0.2;0.7;0.2" dur="3.6s" begin="0.6s" repeatCount="indefinite"/>
          </circle>
        </g>
      </g>
    </g>

    <!-- Text: name + role -->
    <g transform="translate(168,36)" fill="#dffcff" font-family="Segoe UI, Roboto, Arial" >
      <text x="0" y="20" font-size="24" font-weight="700">Ing. José Luis Apaza Quispe</text>
      <text x="0" y="48" font-size="13" fill="#9bd6d1">Telecommunications Engineer · RF · Satcom · Radar · 5G/6G</text>
      <text x="0" y="68" font-size="12" fill="#9bd6d1">PCB & Embedded · AI · IoT · Automation · Cybersecurity · Network Architecture</text>
    </g>

    <!-- subtle accent line -->
    <rect x="160" y="104" width="620" height="2" rx="1" fill="url(#g1)" opacity="0.85" filter="url(#f1)"/>
  </svg>
</p>

<!-- Quick facts (badges) -->
<p align="center">
  <img src="https://komarev.com/ghpvc/?username=Luis130798&label=Visitantes&color=00ffd0&style=flat-square" alt="Visitors" />
  &nbsp;
  <img src="https://img.shields.io/badge/Ubicación-Arequipa%2C%20Peru-00a3ff?style=flat-square&logo=google-maps" alt="location" />
  &nbsp;
  <img src="https://img.shields.io/badge/Followers-2-00ffd0?style=flat-square&logo=github" alt="followers" />
  &nbsp;
  <img src="https://img.shields.io/badge/Disponibilidad-Consultoría-00ffd0?style=flat-square" alt="availability" />
</p>

---

## Sobre mí \ (Resumen ejecutivo)
Ingeniero de Telecomunicaciones con trayectoria en **RF, comunicaciones satelitales, sistemas radar y arquitecturas 5G/6G**. \  
Líder en diseño de soluciones integradas que unen **hardware, software y seguridad**, orientadas a despliegues industriales y operativos a escala. \  
Mi trabajo prioriza **robustez técnica, escalabilidad y transferencia de conocimiento**: publico guías, herramientas y repositorios que otros profesionales usan en producción. \

---

## Áreas de excelencia \ (alto impacto)

- **Sistemas RF & Enlaces Satcom** — planificación, enlace enlace-budget, mitigación de interferencias y coexistencia.  
- **Redes Móviles y RAN** — diseño RAN 4G/5G/6G, integración Core/RAN y testing de KPIs.  
- **Radar & Sensores** — diseño de cadena RF, procesamiento de señal y análisis de detección.  
- **PCB & Embebidos** — diseño RF-aware de PCB, filtros, adaptación de antenas y sistemas con STM32/ESP32.  
- **IoT industrial & Automatización** — topologías resilientes, seguridad por diseño, gateways y orquestación.  
- **Ciberseguridad operacional** — segmentación, IDS/IPS, VPNs y auditoría de infraestructura crítica.

---

## Métricas & Visuales (actuales)
<p align="center">
  <!-- GitHub stats (oscuro, serio) -->
  <img src="https://github-readme-stats.vercel.app/api?username=Luis130798&show_icons=true&theme=gruvbox&hide_border=true&count_private=true" height="140" alt="GitHub Stats" />
  &nbsp;
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Luis130798&layout=compact&theme=gruvbox&hide_border=true" height="140" alt="Top Languages" />
</p>

---

## Diagrama técnico — Visión de una solución satelital 5G / IoT
```mermaid
flowchart TB
  subgraph Edge
    GW[Gateway IoT / Edge Compute]
    SENS[Sensor Nodes]
  end
  subgraph Backhaul
    Sat[Satcom Link]
    NR[5G-NR gNodeB]
  end
  subgraph Core
    UPF[User Plane Function]
    SMF[Session Mgmt]
    NMS[Network Mgmt & Security]
  end

  SENS -->|MQTT/TLS| GW -->|IPsec| Sat --> NR --> UPF --> NMS
  NMS -->|Policy| SMF
  style Sat fill:#0f3c4a,stroke:#00ffd0,stroke-width:1px
  style NR fill:#102028,stroke:#00a3ff,stroke-width:1px
