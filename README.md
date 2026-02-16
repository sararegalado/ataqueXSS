# Práctica 1 - Ataque XSS

Demostración interactiva de vulnerabilidades **Cross-Site Scripting (XSS)** para la asignatura de Seguridad de la Información.

## Descripción

Esta práctica muestra la diferencia entre procesar entrada de usuario de forma vulnerable vs segura:

- **Vulnerable:** usa `innerHTML`, permitiendo la ejecución de código malicioso.
- **Seguro:** usa `textContent` y escapa caracteres especiales HTML.

## Uso

1. Abre `index.html` en un navegador.
2. Introduce un payload de prueba en el textarea.
3. Compara el comportamiento de ambos botones.

## Payloads de ejemplo

```html
<img src=x onerror="alert('XSS')">
<script>alert('XSS')</script>
<img src=x onerror="alert(document.cookie)">
```

## Mitigaciones

- Usar `textContent` en lugar de `innerHTML`
- Sanitizar entrada del usuario
- Implementar Content Security Policy (CSP)
- Validación server-side

---

*Seguridad de la Información · Curso 2025-2026*
