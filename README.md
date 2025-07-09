# Sistema de Reservas - Pruebas Automatizadas

Este proyecto es parte del Bootcamp de Especialización en DevOps, específicamente del Módulo 4: Automatización de Pruebas.

## Descripción

Sistema simple de reserva de habitaciones que permite:
- Verificar disponibilidad de habitaciones
- Crear nuevas reservas
- Rechazar reservas duplicadas (mismo cuarto y hora)

El proyecto sirve como introducción a conceptos básicos de pruebas automatizadas usando pytest y su integración con GitHub Actions para CI/CD.

## Estructura del Proyecto

```
├── app/
│   ├── __init__.py
│   ├── api.py          # API REST con Flask
│   └── reservations.py # Lógica de negocio
├── tests/
│   ├── test_api.py         # Pruebas de la API
│   └── test_reservations.py # Pruebas unitarias de la lógica
└── pytest.ini         # Configuración de pytest
```

## Funcionalidades Probadas

### Lógica de Negocio (`test_reservations.py`)
- `test_available_room`: Verifica que se puede reservar una habitación disponible
- `test_not_available_room`: Verifica que no se puede reservar una habitación ya ocupada

### API REST (`test_api.py`)
- `test_success`: Verifica que una reserva exitosa devuelve código 201
- `test_failure`: Verifica que intentar duplicar una reserva devuelve código 409

## Tecnologías

- **Python**: Lenguaje de programación
- **Flask**: Framework web para la API
- **Pytest**: Framework de pruebas
- **GitHub Actions**: CI/CD para ejecución automática de pruebas

## Cómo Ejecutar las Pruebas

1. **Configurar entorno virtual**
   ```bash
   python -m venv env
   source env/bin/activate  # En Windows: env\Scripts\activate
   pip install -r requirements.txt
   ```

2. **Ejecutar pruebas**
   ```bash
   pytest
   ```

## Objetivos de Aprendizaje

Este proyecto enseña:
1. **Creación de pruebas básicas** con pytest
2. **Separación de responsabilidades** entre pruebas unitarias y de integración
3. **Automatización de pruebas** con GitHub Actions
4. **Principios de CI/CD** para validación continua de código

## Próximos Pasos

- Añadir más casos de prueba
- Implementar pruebas parametrizadas
- Configurar cobertura de código
- Expandir la integración con GitHub Actions

---
*Este proyecto fue creado como parte del Bootcamp de Especialización en DevOps, Módulo 4: Automatización de Pruebas.*
