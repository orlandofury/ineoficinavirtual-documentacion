---
title: Flujo de datos aprobacion de solicitudes y generacion de constancia en Oficina Virtual
https://mermaid-js.github.io/mermaid-live-editor/edit#pako:eNp1UktuwjAQvcrIKyrBBVhUgvApi6ooVF00YTGNB7CUjF3HQaoIh-oZerFOQoho1WY1Sd5n3rNPKrOa1FjtPboDPM9SBnlWSUxZ5T1xoC2MRvf1iveeSqxhkjy9bGxuMhMqDZEn1Li9sCYtco0lAoIj1qbhgybwdDSlsVzDdLD-68fdRWHaKkwYc1MGMYtOcQNA6B3PF2DUAmN6r4QebAkrzmzhcmrmkr4-MUcto7MesJebJTsc73BEfKTcOoJHZI0eIitRrSx9k_ofn96lhnky56MROkIp-lTImstN3DFnHfMqeGWiZL6q1RD_aLPvrNOIO422esDbGi-AeQtoXGFPTB7FhSUqZ0biLga34ui8fZPDajtpKF3ni9-LmsJ5U1ANy0HUq3XgZQOGh2RhWHZUQ1WQL9BouUGnBpGqcKCCUjWWUdMOqzykKuWzQLEKdvPBmRoHX9FQVU5joJlBuXuFknPJS_nqkF-tvb6fvwG2F-Z1
---
```mermaid
graph TD
    I[Recurrente] -->|Ingresa| A[OVSolicitud Creada]
    A -->|Pasa a pendiente de revision| B(Pendiente de revision)
    B -->|Analista| C{Revisa Solicitud}
    C -->|Requisitos Incompletos señalados por analista| D[fa:fa-envelope Mandar Correo a Recurrente]
    C -->|Requisitos completos| E[Enviar a sistema SGSR]
    D -->|Recurrente completa requisitos| R[OVSolicitud pendiente]
    R -->|Regresa a revision| B
    E -->|SGSR genera constancia| F(OVSolicitud aprobada por SGSR)
    F -->|Recurrente imprime| G(Constancia)
    G --> H[Fin]
```
