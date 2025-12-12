# SmartRetail IA – Server Side (API & IA)

Este módulo contiene el **backend de SmartRetail IA**, encargado de:

-   Exponer la **API REST** consumida por la app de Next.js.
-   Gestionar **usuarios, autenticación y sesiones**.
-   Conectar con la **base de datos PostgreSQL**.
-   Ejecutar la lógica de **predicción de demanda** mediante IA (Python + OpenAI + ML clásico).

---

## 🧱 Tecnologías

-   **FastAPI** (Python) – Framework principal de la API.
-   **Uvicorn** – Servidor ASGI.
-   **PostgreSQL** – Base de datos principal.
-   **Prisma Client Python** o SQLAlchemy – Acceso a datos.
-   **Pandas, Scikit-learn** – Procesado y modelos clásicos.
-   **OpenAI API** – IA avanzada para predicción.
-   **PyJWT** – Autenticación basada en tokens.
-   **Docker** – Contenedores para despliegue.

## 🧩 Arquitectura del Módulo

El backend está organizado siguiendo una estructura modular para mantener el código limpio y escalable:

-   /api/ – Endpoints REST divididos por recursos (auth, usuarios, predicción, inventario…).

-   /services/ – Lógica de negocio independiente de los controladores.

-   /models/ – Esquemas de datos, tanto ORM como validación con Pydantic.

-   /ml/ – Scripts y modelos de predicción entrenables, pipelines y utilidades.

-   /database/ – Conexiones, migraciones y configuración del ORM.

-   /utils/ – Funciones auxiliares (logs, emails, hashing, validaciones…).
